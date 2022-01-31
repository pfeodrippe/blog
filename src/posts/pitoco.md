# Pitoco

One project I have been working recently is [Pitoco](https://github.com/pfeodrippe/pitoco), it’s written in Clojure and was originally created with the purpose of inferring REST HTTP requests using packet capture, heavily inspired in a startup called [Akita](https://www.akitasoftware.com/blog). 

The first place where I tested it was in my daily job (Gravie, a healthcare startup company[^gravie]). At Gravie there is a legacy app in Grails (we are migrating/doing new services to/in Clojure) which exposes many REST endpoints and I wanted to understand more what's was there, this happened at the same time as I was reading some awesome posts from the Akita blog and that was the trigger which leaded to this project. Let's see how you could use it in your project.

## Capture packet data
Imagine you have your server for integration or E2E tests at  `localhost:8005`. You have no OpenAPI schema or most of the documentation is outdated, you can start `tcpdump` to capture packet data (which we will see how to process later).

```bash
tcpdump -i lo0 'port 8005' -w lo.pcap
```

In some other terminal you can exercise the endpoints (e.g. by running the tests). When the exercise is finished, stop `tcpdump` run and check that you have a `lo.pcap` file. These are your TCP packets in some binary format (I'm not a network person, so pardon my language)

TODO Another usage was for Cypress tests.

[^gravie]: (we are hiring, send a email to [our CTO](mcameron@gravie.com))