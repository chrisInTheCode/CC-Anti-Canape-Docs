**Anti-Canape was developed to fix a gap between automation needs and application resources**. Many applications that were being used were not efficient or user-friendly enough to support automation, and current automation possibilities were not always convenient to accomplish more-simple actions. Because of this, I began working on Anti-Canape. Anti-Canape started as a project just for reading CAN messages, and then writing CAN messages, and then encoding and decoding CAN messages, and then parsing DBC files, and then writing SDO messages, and then reading SDO messages, then parsing DOT files, then automating testing procedures, and so on and so on. *It's been a constant advancement of python capabilities with CAN communication and is now stable enough to be used both on its own and as part of other applications / frameworks*. 

**Through several revisions, the classes and modules you will find in the project today are a result of changing needs and understandings as to what is needed in the long-term**:  
- It has now extended support for automation and script creation, allowing all of its various features to be implemented in almost every way possible  
- It uses threading in all of its operations, allowing buffers to be stabalized so that no messages are lost  
- It manages cross threads as safely as possible, and ensures that no thread will get cut with the use of thread-safe objects  
- It provides calculations, conversions, and encodings on the backside to ensure that CAN communication is as user-friendly as possible  
- It carries as few dependencies as possible, allowing for a light(er)weight framework to build off of  
- It has lots of in-code and out-of-code documentation and references to support continual development and implementation  
- It makes use of user internalization, being that only a small group of people will ever use this framework, allowing things like DBC and DOT parsers to be possible with Club-Car specialized information and technology  
- It supports CAN communication on a variety of dongles, and includes three default configurations for use with Kvaser, Vector, and PCan dongles in the Club Car Validation Dept  

**The project is now ready to be used for initial test automation with basic CAN signals and SDO parameters**. The only communication protocol currently in use not available with this framework is CCP/XCP communication, which is a planned addition for the future if I ever have the time and resources.

For more project and contact information, please see [the overview](././index.md)

Always a Great Day at The Club!  
- *Chris Hinkson, Original Author 2023*