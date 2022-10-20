[![REUSE status](https://api.reuse.software/badge/github.com/SAP-samples/digital-manufacturing-extension-samples)](https://api.reuse.software/info/github.com/SAP-samples/digital-manufacturing-extension-samples)

# SAP Digital Manufacturing Extension Samples
SAP Digital Manufacturing provides an out-of-the-box Manufacturing Execution System (MES) to run production on the shop floor. However, based on the experience gained from customer and partner projects, we also know that a successful MES must have the capability to be extended. With the new releases of Digital Manufacturing Cloud, the options for extensibility have made a significant step forward. Using the sample extensions provided will allow you to learn and understand how to build your own extensions to use with SAP Digital Manufacturing Cloud.

# Extensibility by Use case

| Scenario      | Description   | DMC Extension Pattern(s)   | <div style="width:360px">Blogs</div>          |
| ------------- | ------------- | ------------- | ------------- |
| 1 | Integrating additional fields from ERP <br/> during master data integration to DMC | Integration Extension, Field Extension | [Integration Extension with S/4HANA Part 1](https://blogs.sap.com/2021/08/24/sap-digital-manufacturing-cloud-integration-extension) <br/> [Integration Extension with S/4HANA Part 2](https://blogs.sap.com/2021/09/21/sap-digital-manufacturing-cloud-integration-extension-part-ii) <br/>  [Integration Extension with S/4HANA Cloud](https://blogs.sap.com/2021/02/05/use-sap-cloud-platform-integration-for-mediated-integration-between-sap-s-4hana-cloud-and-sap-digital-manufacturing-cloud) |
2 | Showcasing the custom Fields from ERP <br/> in a custom POD plugin | POD Extension | [Building POD Extension easy way](https://blogs.sap.com/2022/04/11/building-a-custom-digital-manufacturing-cloud-pod-plugin-the-easy-way) <br/> [View Plugin](https://github.com/SAP-samples/digital-manufacturing-extension-samples/blob/main/DMC_UIExtensions/ViewPodPluginTemplate_And_Example/documentation/InstallationAndConfigurationGuide.pdf) <br/> [Execution plugin](https://github.com/SAP-samples/digital-manufacturing-extension-samples/blob/main/DMC_UIExtensions/ExecutionPodPluginTemplate_and_Example/documentation/InstallationAndConfigurationGuide.pdf) |
3 | Visual Inspection | Bring your own ML Model | [Visual Inspection Overview](https://blogs.sap.com/2020/12/14/ai-ml-solution-for-visual-inspection-overview-how-to-close-the-production-gap-for-machine-learning/) <br/>  [End to end ML Scenario](https://blogs.sap.com/2022/07/10/end-to-end-ai-ml-scenario-configuration-in-sap-dmc/) <br/> [Inspection at the speed of sight](https://sapvideoa35699dc5.hana.ondemand.com/?entry_id=1_p3ss7uhx)   |
4 | Simplified action buttons for operators and Process automation  | Process Extension | [Calling BTP Workflow Services](https://blogs.sap.com/2022/07/22/sap-digital-manufacturing-cloud-process-extension-integrated-with-sap-workflow-management/) <br/> [Collaboration with Microsoft Team](https://blogs.sap.com/2021/09/17/integrating-microsoft-teams-with-sap-digital-manufacturing-cloud/) |
5 | Managing numbering pattern with specific requirements  | In-App Extension | [Next Numbers](https://github.com/SAP-samples/digital-manufacturing-extension-samples/blob/main/DMC_NextNumber_InAppExtensions/batch-nn-postgresql/documentation/InstallationAndConfigurationGuide.pdf) |
6 | Template Assembly POD | Side by side Extension | |
7 | Linking SAC Stories in DMC | KPI Extension | [SAC stories in DMC](https://blogs.sap.com/2021/11/16/dashboard-designer-embedding-sap-analytics-cloud-sac-stories-into-sap-digital-manufacturing-cloud-dmc-dashboards/) |
8 | Custom ME POD | ME Extension | [SAP ME UI5 Extension POD](ME_POD) |


## DMC Extension Patterns
In SAP Digital Manufacturing we distinguish between the following major areas for extensions:

 - **In-App Extensions**
 - **Process Extensions**
 - **POD Extensions**
 - **Field Extensions**
 - **Side by Side Extensions**
 - **Integration Extensions**
 - **KPI Extensions**
 - **Machine Learning Extensions**

![](docs/assets/indexLectureSlide31.png)

## Note
Our recommended extensibility platform for DMC is Kyma, however, it can be use case specific which may lead into different recommendations. Please know that DMC extensions can also be done with Cloud Foundry using a PaaS environment (or hyperscaler options which have not been fully explored).  The main difference picking between these two options, outside of our recommendation, is the lifecycle and costs. Kyma takes care of the lifecycle, scalability, monitoring, deployment, etc. of the extensions but is more expensive while Cloud Foundry/PaaS will have lower upfront costs but can be costly in terms of complexity, time, etc. to implement lifecycle management separately.



## Real World Customer Examples
![](docs/assets/indexLectureSlide33.png)
![](docs/assets/indexLectureSlide34.png)
![](resources/images/me_ext_pod.png)

## How to obtain support
If you have issues with a sample, please open a report using [GitHub issues](../../issues).

## License
Copyright © 2020 SAP SE or an SAP affiliate company. All rights reserved. This project is licensed under the Apache Software License, v2.0 except as noted otherwise in the  [LICENSE](LICENSES/Apache-2.0.txt).
