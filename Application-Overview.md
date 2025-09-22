## Application Overview

The To Do application supports the following functionality:

   * [To Do Items](/Application-Overview/Application-Items.md)
   * [Application Maintenance](/Application-Overview/Application-Maintenance.md)
   * [User Management](/Application-Overview/Application-Users.md)
   * [Application Setup](/Application-Overview/Application-Setup.md)
   * [Azure DevOps Configuration](/Application-Overview/Application-DevOps.md)


The to do items, categories, priorities, and users are arranged in the database like this:

   ![entity-relationship-diagram](/.attachments/application-erd.png)

   *Figure 1 - Entity Relationship Diagram*

Initially, it is recommended that the following multiplicity be maintained:
    * Every user can have zero or more to do Items
    * Every user has one Role
    * Every to do Item has one Category
    * Every to do Item has one Priority
