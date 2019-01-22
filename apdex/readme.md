# Application Performance Index

Apdex is a measure of response time based against a set threshold. It measures the ratio of satisfactory response times to unsatisfactory response times. The response time is measured from an asset request to completed delivery back to the requestor.

The application owner defines a response time threshold T. All responses handled in T or less time satisfy the user.

For example, if T is 1.2 seconds and a response completes in 0.5 seconds, then the user is satisfied. All responses greater than 1.2 seconds dissatisfy the user. Responses greater than 4.8 seconds frustrate the user.

Apdex tracks three response counts:

Satisfied: The response time is less than or equal to T.
Tolerating: The response time is greater than T and less than or equal to 4T. In this example, 4 x 1.2 = 4.8 seconds as the maximum tolerable response time.
Frustrated: The response time is greater than 4T.
Your configuration file's apdex_f value is four times your app server's Apdex T value. This threshold is useful, for example, with transaction traces. For more information, see the configuration file documentation for your New Relic agent.

The Time calculation will change based on your own app's T setting. In the following example, T = 1.2 seconds.
