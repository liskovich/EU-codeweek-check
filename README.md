**Short intro into app structure**

*src contains:*
- API - retrieve and save to server
- Application - Abstracrions (interface) for application logic, depends only on *Domain* (Common, Entities named folders, DI)
- Domain - store enterprise wide things 
(types, entities, exceptions, common, enums, events, ValueObjects), does not depend on anything
- Infrastrucuture - concrete implementation for abstractions defined in *Application* 
(DB access, identity, Services, DI)
- WebDashboard - access to system (for business owners). Depends on *Application* and *Infrastructure* 
(only to be used in service registration part)

*mobile contains:*
- mobile app for Android (students)
- mobile app for iOS (students)