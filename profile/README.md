# William Belle LLC

I deploy apps built with AI tools to Azure and keep them running.
[williambelle.co](https://williambelle.co)

What is public here is the software that gets installed into a client's app.

## The agents

| Stack | Package | Source |
| --- | --- | --- |
| .NET | [`WilliamBelle.Monitoring`](https://www.nuget.org/packages/WilliamBelle.Monitoring) | [`williambelle-monitoring-dotnet`](https://github.com/williambelle-co/williambelle-monitoring-dotnet) |
| Node | [`@williambelle-co/monitoring`](https://www.npmjs.com/package/@williambelle-co/monitoring) | [`williambelle-monitoring-node`](https://github.com/williambelle-co/williambelle-monitoring-node) |

Both report, on a schedule, what only the inside of a running deployment can
see: the runtime it is actually on, the environment it thinks it is in, and the
package versions actually installed. A repository can say a vulnerable package
was upgraded while production still runs the old version. This is what notices.

They speak the same wire protocol and report to the same endpoint, so an
application built out of both lands in one place.

Neither accepts inbound anything: no endpoint, no commands, no remote
configuration, no code execution. Neither collects logs, request payloads, or
user data. Each README lists the complete set of fields sent, and both are
licensed MIT, so you can check that against the source before installing
either.

## Installing one

Each application needs an id and a signing key, issued per application. Write to
[support@williambelle.co](mailto:support@williambelle.co) for those, or with a
question about an application already reporting.
