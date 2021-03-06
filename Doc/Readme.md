# Real-Time KQL Command Line Tool

Real-Time KQL allows users to examine activity on their machine by directly viewing and querying real-time event streams. Unlike most other tools that offer a similar capability, Real-Time KQL allows a user to begin event processing **as and when events arrive, in real time**.

For instance, suppose a user wanted to see if there was an adversary trying to login into their computer simply by guessing different passwords repeatedly (brute-force). This user could then, for example, use Real-Time KQL to filter through 1000s of events and see only the instances where an adversary has attempted to login into their machine 3 or more times in a 30 second window.

See the [query guide](QueryGuide.md) for more information on how to accomplish tasks like the one mentioned above.

This diagram shows an overview of how Real-Time KQL works:

![StandingQuery.jpg](StandingQuery.jpg)

A user can specify the input and output sources as well as any query files to apply to the given input stream. Real-Time KQL will process the event stream and output the result.

[**Get started**](GettingStarted.md) using Real-Time KQL.

### Demos and Documentation

|                         |                           Windows                            |                            Linux                             |
| :---------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
|       **OS Logs**       | **WinLog** - logs seen in EventVwr or log file(s) on disk<br />[Doc](Winlog.md) / [Demo](https://youtu.be/GoTSuWPrkig) | **Syslog** - the OS log<br />[Doc](Syslog.md) / [Demo](https://youtu.be/kw6bSGolnpU) |
| **High-Volume Tracing** | **Etw** - Event Tracing for Windows<br />[Doc](Etw.md) / [Demo](https://youtu.be/1UOL1Sg7puQ) | **EBPF** - dynamic interception of kernel and user mode functions<br />*Coming soon* |



### Query Files

Check out the [query writing guide](QueryGuide.md) for some best practices on coming up with queries for Real-Time KQL.



### Output Options

|                       Real-Time Output                       |                         File Output                          |                        Upload Output                         |
| :----------------------------------------------------------: | :----------------------------------------------------------: | :----------------------------------------------------------: |
| [consoleOutput](RealTimeOutput.md#ConsoleOutput) - Results printed to standard output | [jsonOutput](FileOutput.md#JSONOutput) - Each event is a JSON dictionary | [adxOutput](UploadOutput.md#ADXOutput) - Upload to Kusto (Azure Data Explorer) |
| **webEvents** - Real-Time KQL acts as real-time server for events. | **csvOutput** - Each event is a row in Comma Separated Value table | [blobStorage](UploadOutput.md#BlobStorage) - Upload as JSON objects to BlobStorage |
|                                                              | **htmlOutput** - Each event formatted as human-readable DIV element |                                                              |