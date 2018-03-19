# Multi Tenancy Applications

To define a multi-tenancy application, take npm as an example. npm has organisations and npm Enterprise.

Organisations allow you to have private packages, but everyone's packages are served by the same registry. By contrast, each purchaser of Enterprise has their own npm and it's self-hosted by the purchaser.

Organisations are multi-tenancy as everyone uses the same instance but each only access to their own data in that instance. Enterprise is single-tenancy as each customer has it's own npm, so to speak.

Websites like Twitter, Instagram etc. aren't to be considered multi-tenancy as although everyone likely share's the same database, they aren't portioning off their data. They all have the same experience and there isn't any custom configuration.

Another example of a multi-tenancy application might be something like Vogue. US and UK Vogue have the same requirements, but they'll have different articles. Host them in the same application but keep their data separate.

They can have their own branding but being hosted on the same server allows you to keep both site's software up to date and reduces server costs as they don't need their own server. It's easier to scale up, and having all data in one place makes it easier us for analyse data and spot trends.

A downside of a multi-tenancy application is that if the instance goes down, all users of that instance go down too. UK Vogue goes down? So does US.

A multi-tenant application is also more complex to build, particularly in ensuring that each instance doesn't share eachothers cache. Data leakage is bad, y'all.

