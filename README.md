[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/digital-manufacturing-extension-samples)](https://api.reuse.software/info/github.com/SAP-samples/digital-manufacturing-extension-samples)

# SAP Digital Manufacturing Extension Samples
SAP Digital Manufacturing provides an out-of-the-box Manufacturing Execution System (MES) to run production on the shop floor. However, based on the experience gained from customer and partner projects, we also know that a successful MES must have the capability to be extended. With the new releases of Digital Manufacturing Cloud, the options for extensibility have made a significant step forward. Using the sample extensions provided will allow you to learn and understand how to build your own extensions to use with SAP Digital Manufacturing Cloud.

## Description
In SAP Digital Manufacturing we distinguish between the following major areas for extensions:

**In-App Extensions**

The ability to extend a core DMC application* by the available extension points (e.g. extend existing API, trigger a parallel processes, augment API outputs,…etc.). This spectrum of this extensibility use case can go from simple to complex if the logic of the extension needs to call API’s from DMC. 

If the extension is emulated in DMC PaaS account, the infrastructure will have to be managed separately including scaling, deploying,...etc. while in the Kyma Runtime environment it’s fully SAP managed.

*Limited DMC application support today for this use case

Personas: 

- Software Developer

**Process Extensions** 

An extension that will be called from the DMC Production Process Designer process flow that will be executed in the DMC Process Engine (PE) (e.g. extension could trigger a parallel process in an external system, augment the core process flow,…etc.).  Provides flexibility to adapt processes within and outside DMC.

The extension point is usually triggered manually by an operator from the production operator dashboard or triggered from machines automatically as a subscription.

Personas:

- Business User
- Software Developer (NodeJs, Microservices)

**POD Extensions** 

A custom plug-in extension to the DMC Production Operation Dashboard (POD).  DMC will treat the custom plugin as it it’s a core plugin (e.g. automatically participates in the overall  lifecycle of the POD and receives all appropriate messages).

The application can be built using local editors such as Visual Studio Code. 

Personas:

- Software Developer (JavaScript, UI5)

**Field Extensions**

Adding custom fields to DMC applications fields.

Personas:

- Business User


**Side by Side Extensions**

Develop a separate side by side custom application, including a UI, that can be integrated via public APIs and extensions with DMC.

The application can be built using local editors such as Visual Studio Code. 

Personas:

- Software Developer

**Integration Extensions**

DMC utilizes SAP Integration to integrate with external and other SAP Systems. Customer can utilize predefined  iflows for various systems for the transformation of data. Alternative customers can  develop their own or enrich existing ones. iflows nodes use XSLT or custom developed exits to transform data into the required format.

The flows can be augmented with custom extensions written by a developer in the case the iflows are not capable of transforming the date to the desired format, or other data are needed to enrich the existing data.

Personas:

- Software Developer
- Business User

**KPI Extensions**

Provides the flexibility to build complex KPI calculation logic that are specific to the customer and integrates with DMC to be aggregated at various levels of the enterprise hierarchy and visualized in DMC-Dashboard Designer.

Personas:

- Software Developer
- Business Consultant

**Machine Learning Extensions**

Bring you own ML model trained on any ML service/tool and deploy it with DMC and integrate it to the business & manufacturing processes without a line of code.

The ML model can be trained with common ML services/tools but needs to be exported or converted into TensorFlow JavaScript ML model binary files. Please check release notes for further updates on supported ML formats.

Personas:

- Business User
- Citizen Data Scientist

![](docs/assets/indexLectureSlide31.png)

## Note
Our recommended extensibility platform for DMC is Kyma, however, it can be use case specific which may lead into different recommendations. Please know that DMC extensions can also be done with Cloud Foundry using a PaaS environment (or hyperscaler options which have not been fully explored).  The main difference picking between these two options, outside of our recommendation, is the lifecycle and costs. Kyma takes care of the lifecycle, scalability, monitoring, deployment, etc. of the extensions but is more expensive while Cloud Foundry/PaaS will have lower upfront costs but can be costly in terms of complexity, time, etc. to implement lifecycle management separately.

## DMC Extensibility by Use case

| Scenario      | Description   | DMC Extension Pattern(s)   | <div style="width:360px">Blogs</div>          |
| ------------- | ------------- | ------------- | ------------- |
| 1 | Integrating additional fields from ERP <br/> during master data integration to DMC | Integration Extension, Field Extension | [Integration Extension with S/4HANA Part 1](https://blogs.sap.com/2021/08/24/sap-digital-manufacturing-cloud-integration-extension) <br/> [Integration Extension with S/4HANA Part 2](https://blogs.sap.com/2021/09/21/sap-digital-manufacturing-cloud-integration-extension-part-ii) <br/>  [Integration Extension with S/4HANA Cloud](https://blogs.sap.com/2021/02/05/use-sap-cloud-platform-integration-for-mediated-integration-between-sap-s-4hana-cloud-and-sap-digital-manufacturing-cloud) |
2 | Showcasing the custom Fields from ERP <br/> in a custom POD plugin | POD Extension | [Building POD Extension easy way](https://blogs.sap.com/2022/04/11/building-a-custom-digital-manufacturing-cloud-pod-plugin-the-easy-way) <br/> [View Plugin](https://github.com/SAP-samples/digital-manufacturing-extension-samples/blob/main/DMC_UIExtensions/ViewPodPluginTemplate_And_Example/documentation/InstallationAndConfigurationGuide.pdf) <br/> [Execution plugin](https://github.com/SAP-samples/digital-manufacturing-extension-samples/blob/main/DMC_UIExtensions/ExecutionPodPluginTemplate_and_Example/documentation/InstallationAndConfigurationGuide.pdf) |
3 | Visual Inspection | Bring your own ML Model | [Visual Inspection Overview](https://blogs.sap.com/2020/12/14/ai-ml-solution-for-visual-inspection-overview-how-to-close-the-production-gap-for-machine-learning/) <br/>  [End to end ML Scenario](https://blogs.sap.com/2022/07/10/end-to-end-ai-ml-scenario-configuration-in-sap-dmc/) <br/> [Inspection at the speed of Sight](https://sapvideoa35699dc5.hana.ondemand.com/?entry_id=1_p3ss7uhx)   |
4 | Simplified action buttons for operators and Process automation  | Process Extension | [Calling BTP Services](https://blogs.sap.com/2022/07/22/sap-digital-manufacturing-cloud-process-extension-integrated-with-sap-workflow-management/) <br/> [Collaboration with Microsoft Team](https://blogs.sap.com/2021/09/17/integrating-microsoft-teams-with-sap-digital-manufacturing-cloud/) |
5 | Managing numbering pattern with specific requirements  | In-App Extension | [Next Numbers](https://github.com/SAP-samples/digital-manufacturing-extension-samples/blob/main/DMC_NextNumber_InAppExtensions/batch-nn-postgresql/documentation/InstallationAndConfigurationGuide.pdf) |
6 | Template Assembly POD | Side by side Extension | |
7 | Linking SAC Stories in DMC | KPI Extension | [Next Numbers](https://blogs.sap.com/2021/11/16/dashboard-designer-embedding-sap-analytics-cloud-sac-stories-into-sap-digital-manufacturing-cloud-dmc-dashboards/) |
8 | Custom ME POD | ME Extension | [SAP ME UI5 Extension POD](ME_POD) |

## Real World Customer Examples
![](docs/assets/indexLectureSlide33.png)
![](docs/assets/indexLectureSlide34.png)

With the new release of SAP ME 15.4, all the PAPIs are exposed as REST API’s which enables SAPUI5 based extensions of Production Operator Dashboards (POD) without SAP ME Software Development Kit (SDK).<br /> Using the sample extensions provided will allow you to learn and understand how to build your SAPUI5 based extensions of Production Operator Dashboards to use with SAP ME.
![](resources/images/me_ext_pod.png)

## How to obtain support
If you have issues with a sample, please open a report using [GitHub issues](../../issues).

## License
Copyright © 2020 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, v2.0 except as noted otherwise in the  [LICENSE](LICENSES/Apache-2.0.txt).
