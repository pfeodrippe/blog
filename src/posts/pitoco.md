# Pitoco

One project I have been working recently is [Pitoco](https://github.com/pfeodrippe/pitoco), it’s written in Clojure and was originally created with the purpose of inferring REST HTTP requests using packet capture, heavily inspired in a startup called [Akita](https://www.akitasoftware.com/blog). 

The first place where I tested it was in my daily job (Gravie, a healthcare startup company[^ gravie]). At Gravie there is a legacy app in Grails (we are migrating/doing new services to/in Clojure) which exposes many REST endpoints and I wanted to understand more of it, at the same time I was reading some awesome posts from Akita and that was the trigger which lead to this project.

[^ gravie]: (we are hiring, send a email to [our CTO](mcameron@gravie.com))

TODO Another usage was for Cypress tests.