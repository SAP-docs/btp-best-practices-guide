<!-- loio50a7c7d65c8a458bacb401a95c9ce976 -->

# Performing UI, Usability, and Unit Tests

You should always conduct careful testing to ensure that your application is of high quality. Create a release candidate to propagate throughout your landscape.

For example, consider testing the user interface, usability, and performance, as well as running general unit tests. Developers should use unit tests to ensure that software modules behave as expected. Unit tests are the smallest tests, and they detect issues fast. Taking good care of unit tests usually leads to better maintainable and understandable code. If you use the Continuous Integration process, you should consider automated tests as part of the pipeline.



<a name="loio50a7c7d65c8a458bacb401a95c9ce976__section_crp_5qc_wgb"/>

## SAPUI5

SAPUI5 supports QUnit testing. We recommend that you write unit tests as small as possible, ensuring that you only test one single thing at a time. This will not only make debugging easier, but also maintaining the tests in the long run.

For an overview of available testing options for SAPUI5 developments, see [Testing and Performance Measurement](https://sapui5.hana.ondemand.com/#/topic/291c9121e6044ab381e0b51716f97f52).

For SAPUI5 and SAP Fiori testing, please see the demokit for SAP UI5: [https://sapui5.hana.ondemand.com/\#/topic](https://sapui5.hana.ondemand.com/#/topic).



## SAP Cloud SDK

We recommend that you write JUnit tests for the modules of your backend services. They should be very granular in that they only test individual modules, such as a class. See [Step 13 with SAP Cloud SDK: Automated Testing](https://blogs.sap.com/2017/09/19/step-12-with-sap-s4hana-cloud-sdk-automated-testing/).

As part of the Continuous Integration and Delivery Process, we recommend that you run performance tests in SAP Cloud SDK Pipeline to determine the behavior of the software system and change in responsiveness under simulated load conditions. SAP Cloud SDK Pipeline has integrated support for performance tests using JMeter and Gatling. See [Step 23 with SAP Cloud SDK: Performance Tests](https://blogs.sap.com/2018/01/11/step-23-with-sap-s4hana-cloud-sdk-performance-tests/).



<a name="loio50a7c7d65c8a458bacb401a95c9ce976__section_ldg_b4f_xgb"/>

## Testing in SAP Web IDE

SAP Web IDE empowers developers to test and evaluate the functionality and performance of their apps:

-   Use the application preview to test functionality, design and performance before deploying it. There are different configuration options available, such as SAP UI5 runtime version, URL parameters. See [Running Applications in Development Mode](https://help.sap.com/viewer/825270ffffe74d9f988a0f0066ad59f0/CF/en-US/fcc3b671ca084c8ab5e009bd4de19048.html).

-   Run your application using a client mock server. See [Run Applications with Mock Data](https://help.sap.com/viewer/825270ffffe74d9f988a0f0066ad59f0/CF/en-US/e7d047a743b74b83875c3ede20783f24.html).

-   Execute unit tests for SAPUI5 \(Qunit\) and Java \(JUnit\). See [Developing Application Tests](https://help.sap.com/viewer/825270ffffe74d9f988a0f0066ad59f0/CF/en-US/3655fba62f884e84a774c6030eeeab49.html) and [Test a Java Module](https://help.sap.com/viewer/825270ffffe74d9f988a0f0066ad59f0/CF/en-US/25cd7ef4cb8b4e03aaa60ab197cf51b1.html).

-   Execute SAPUI5 integration tests based on OPA5. See [Performing Integration Tests](../integrate-and-test/Integrate_and_Test_84ddc25.md#loio998fbbb1a53c4fbb888e9b14892b3c0c).


