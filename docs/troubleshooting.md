This section outlines a few troubleshooting tips and common snags when using the SparkFun LTE GNSS FUnction Board - SARA-R5.



### LTE Network Availability

The SARA-R5 supports LTE-M and NB-IoT data communication for multi-regional use. Please check the LTE signal availability for your area before purchasing a SARA-R5 product and selecting an LTE service provider / operator.



### Data Connectivity

When working through the data connectivity examples, it is important that you run examples 13, 14 and 17 in order, before moving on to example 18 or 19. Each example builds on the last and together they configure the SARA’s data connection correctly.



### Arduino Debug Messages

If you run into any trouble using one of the Arduino examples, uncomment this line:

    assetTracker.enableDebugging(SERIAL_PORT);

This enables serial debugging to print out the full debug report from AT commands sent via functions in the library. Read through the data and search for matching error codes in Appendix A of the AT Command Reference manual to decipher the code.
