# DevAPIX
API Productization and Developer Collaboration Platform

# Modules
1) Signup/ login
2) API publishing with documentation
3) Free / Paid API Access
4) API Sandbox Testing Tool
5) Project Upload
6) Inviting people
7) Project Contribution
8) Contribution Tracking
9) Project Discussion / Doubt Forum

# Features
## Signup/ login
- Spring Security 6
- BCrypt password hashing
- JWT + Refresh Token
- Role-Based Access Control (RBAC)
- CSRF protection
- HTTPS secure cookies
- Input validation
- security headers
## API publishing with documentation
- Types of api uploading : REST API (optional: GraphQL APIs,Webhooks,Microservice Endpoints) concepts---> transaction ,logging,dtp, validation
- Basic API Details (API Name, Description, Category, Version,Base url, Visibility (Public / Private / Paid)) 
- API Definition (Upload file (yaml, json),Paste Swagger URL) concepts--->(swagger parser, logging, exception)
- Authentication Details ( JWT token)
- sample request and response from the swagger or schema generate ( jackson)
- Headers and parameters (dto)
- status code get from the docs ( enum + dto+ exception handling)
- Search and category-based API discovery ( pagination + sort + filter)
  
