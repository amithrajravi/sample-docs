# APIMAN - API MANAGEMENT

## 1. About this tutorial

### 1.1 Scope

This tutorial contains important notes and instructions about the API management system (**APIMAN**).

### 1.2 Revision history

| Revision | Supported Release | Date | Description |
| :--- | :--- | :--- | :--- |
| A | 1.0 | November 2021 | APIMAN (Initial) |

### 1.3 Intended Audience

This tutorial is primarily intended for **Developer/Engineers** who want to implement API management.

## 2. Introduction to API management

This chapter introduces you to the concept about APIs and how Apiman works currently in the enterprise software ecosystem.

### 2.1 What is an API?

**Application Programming Interface (API)** is a set of protocols for a software application to communicate with another application.

### 2.2 What is API management?

**API management** is the process of enabling an enterprise to manage, control, and provide greater visibility over the APIs owned by them.

The following are the major features:
* Configure governance policies
* Track APIs and its consumers
* Discover and share APIs

### 2.3 Who uses API management?

The following are the primary users of an API management system:
* **API Providers**
* **API Consumers**
* **API Management Administrators**
* **API Developers**

### 2.4 What is Apiman?

**Apiman** is an **open-source API management system**. The following are the two major components of Apiman:

* **API Manager**: It allows **API Providers** to manage their APIs using a web UI. API Providers can define API contracts for their APIs, apply these contracts to multiple APIs, control role-based user access, and control API versions. Using these contracts, API Providers can govern the access to their APIs and define the permissible limit at which the **API Consumers** can access these APIs. API Manager also allows API Consumers to track and access APIs.
* **API Gateway**: It allows the API Providers to apply the contract policies configured during the API management. It generally acts as a gateway between the API and the Client. The API Consumer accesses the API through a URL, which makes the API Gateway a proxy for the API.

### 2.5 Why Apiman is needed?

With the growth of APIs, it becomes very essential for API Providers and API consumers to make best use of the APIs by managing, controlling, and tracking them.

Following are some of the reasons why API management using Apiman is vital:
* **Security**
* **Throttling**
* **Metering**

## 3. Installing Apiman in WildFly 10

This chapter provides instructions about how to download and install the latest version of Apiman and run **WildFly 10**.

### 3.1 Overview

Apiman primarily targets **WildFly 10** as its runtime environment. To install Apiman, you must download both WildFly 10 and the Apiman overlay distribution. Once both are downloaded, you can unpack them in the same location.

### 3.2 Prerequisites

Before you begin with the installation the following conditions must be met:
* You need to have **Java version 1.7 or newer** installed in your system.
* You need to have **WildFly 10** downloaded.
    ```bash
    curl [http://download.jboss.org/wildfly/10.1.0.Final/wildfly-10.1.0.Final.zip](http://download.jboss.org/wildfly/10.1.0.Final/wildfly-10.1.0.Final.zip) -o wildfly-10.1.0.Final.zip
    ```
* You need to have **Apiman 1.3.1.Final** downloaded.
    ```bash
    curl [http://downloads.jboss.org/apiman/1.5.5.Final/apiman-distro-wildfly10-1.5.5.Final-overlay.zip](http://downloads.jboss.org/apiman/1.5.5.Final/apiman-distro-wildfly10-1.5.5.Final-overlay.zip) -o apiman-distro-wildfly10-1.5.5.Final-overlay.zip
    ```

### 3.3 Procedure

Perform the following steps:

1.  Unpack both the downloaded files in the same location.
    ```bash
    unzip wildfly-10.1.0.Final.zip
    unzip -o apiman-distro-wildfly10-1.5.5.Final-overlay.zip -d wildfly-10.1.0.Final
    ```
2.  The Apiman overlay contains what is needed to run Apiman:
    * Apiman binaries (several WAR files)
    * Apiman-specific WildFly 10 configuration (standalone-apiman.xml)
    * Apiman RDBMS datasource (h2)
    * Pre-configured admin user with password **admin** or **admin123!**
    * Pre-configured h2 database for the API Manager (populated with default values)
    * Embedded Elasticsearch instance for metrics and gateway storage

    Therefore, no additional configuration is required to run Apiman.

3.  Run WildFly 10 by using the following Apiman configuration file:
    ```bash
    cd wildfly-10.1.0.
    ./bin/standalone.sh -c standalone-apiman.xml
    ```
4.  Point your browser at the **Apiman UI** and login with the password **admin** or **admin123!**. We strongly recommend you to change the admin password after your initial login.

## 4. Getting Started with Apiman

Apiman is a web-based API management tool that allows you to add an extra layer of access control functionality to an API service. It is used to add authentication or IP filtering to control consumer access, to limit the number of consumer requests within a given time by setting quotas, to analyze usage metrics, and so on.

This tutorial will guide you through the basic configurations of an **API Provider** and an **API Consumer**.

> **Important**: The resulting environment after the installation will have default configurations. It will not solve any security issues that must be considered before production deployment.

### 4.1 Prerequisites

The following conditions must be met:
* You need to have **Apiman installed**.
* You need to have **echo-service quickstart** for demo implementation.
* You need to have a **HTTP client like curl** to test the configured policy.
* You need to have **Maven installed**.

### 4.2 Preparing an echo service

1.  Clone the `apiman-quickstarts` repository or download it as zip and unpack.
2.  Build it with Maven.
    ```bash
    mvn clean install
    ```
3.  Launch the service locally.
    ```bash
    mvn jetty:run
    ```

### 4.3 Logging in to Apiman

1.  Open the **Apiman UI** in your browser.
2.  Enter the username as **admin** and password as **admin** or **admin123!**. You will see the Apiman welcome screen.

### 4.4 Configuring an API Provider

Perform the following steps to configure an API Provider.

#### 4.4.1 Creating an organization

An **organization** is the most basic entity in Apiman. Perform the following steps to create an organization:

1.  In the Apiman welcome screen, navigate to the **Organizations** section.
2.  In the Organizations section, click the **Create a New Organization** link. The New Organization dialog opens.
3.  In the New Organization dialog, enter an organization name and a short description.
4.  Select **Create Organization** to create a new organization. You will see the newly created organization's screen.

#### 4.4.2 Creating a plan

A **plan** contains policies, which are applied by the API Gateway at runtime when requests are made to the API. Perform the following steps to create a plan:

1.  In the Organization screen, select the **Plans** tab. The Plans tab opens.
2.  In the Plans tab, click **New Plan**. The New Plan dialog opens.
3.  In the New Plan dialog, enter a plan name and a short description.
4.  Select **Create Plan** to create a new plan. You will see the newly created plan, and you can now add policies to this plan.

**Adding a policy**

Perform the following steps to add a policy to the plan:

1.  In the Plan Policies screen, click **Add Policy**. The Add Policy dialog opens.
2.  In the Add Policy dialog, select **Quota Policy** from the Policy Type drop-down list and set the quota parameters.
3.  Click **Add Policy** to add the policy to the plan.
4.  Click **Lock Plan** to lock the plan and enable it for use in a contract with an API Consumer.

#### 4.4.3 Adding an API

Perform the following steps to add an API:

1.  In the Organization screen, select the **Services** tab. The Services tab opens.
2.  In the Services tab, click **New Service**. The New Service dialog opens.
3.  In the New Service dialog, enter a service name (**API name**) and a short description.
4.  Click **Create Service** to create a new API. You will see the newly created API's screen.

**Configuring an API**

Perform the following steps to configure an API:

1.  In the API screen, select the **Implementation** tab in the left pane. The Implementation tab opens.
2.  Enter the endpoint (URL) of the local echo-service instance: `http://localhost:9999/apiman-echo`
3.  Select the **API type** from the API Type drop-down list and click **Save** to save the settings.
4.  Select the **Plans** tab to assign a plan to the API and click **Save** to save the settings.
5.  Select the **Overview** tab and click **Publish** to publish the API to the API Gateway. You will see the status of the API is changed to **PUBLISHED** and becomes available now.

### 4.5 Configuring an API Consumer

Perform the following steps to configure an API Consumer. (Repeat similar steps used for creating an organization, plan, policies, contracts, and so on, as in the Configuring an API Provider section).

#### 4.5.1 Creating a Client app

1.  In the Organization screen, select the **Applications** tab. The Applications tab opens.
2.  In the Applications tab, click **New App**. The New App dialog opens.
3.  In the New App dialog, enter a **Client app name**.
4.  Click **Create App** to create a new Client app. You will see the page of your newly created client app’s screen.

#### 4.5.2 Searching an API

Perform the following steps to search an API:

1.  In the **Overview** tab of the client app screen, click **Search for services to consume**. The Find a Service dialog opens.
2.  In the Find a Service dialog, enter the API name in the search bar and click **Search**. You will see a list of APIs based on your search criteria.

#### 4.5.3 Creating a contract

Perform the following steps to create a contract:

1.  In the **Overview** tab of the Client app screen, click **Create a new Service Contract for this Application**. The Service Details dialog opens.
2.  In the Service Details dialog, select the required plan in the **Available Plans** section and click **Create Contract**. The New Contract dialog opens.
3.  In the New Contract dialog, enter the API name in the **Find a Service** field and click **Search**.
4.  Select the API from the displayed list.
5.  Select **Create Contract** to create a contract between the API and the Client app.
6.  Select **I Agree** to agree to the Terms and Conditions of the contract.
7.  In the **Overview** tab of the Client app screen, click **Register**.

Now a **unique key is generated** and the API Consumer can access the API.