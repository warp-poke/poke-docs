# Poke Warp10 Data Model

## Labels semantique

| Name      | Description           | Example                           | Set by    |
|-----------|-----------------------|-----------------------------------|-----------|
| <span style="color:#C2024F">domain</span>    | User domain           | www.domain.tld                    | checker   |
| <span style="color:#04BBBF">path</span>      | URI                   | https://www.domain.tld/poke.pl    | checker   |
| <span style="color:#D2D945">host</span>      | Checker host          | 1.http.gra.checker.poke.io        | checker   |
| <span style="color:#FCB13F">zone</span>      | Availability zone     | eu-west                           | checker   |
| <span style="color:#FF594F">user</span>      | User UUID             |                                   | token     |
| <span style="color:#721BC2">service</span>   | Service UUID          |                                   | token     |

## Checkers

### HTTP

#### Response Status

HTTP Response status (200, 500, …) according to HTTP Specification.

> http.response.status{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#04BBBF">path</span>,<span style="color:#FCB13F">zone</span>}

#### Response Time

HTTP Response time in ms. Time to load the targetted resource.

> http.response.time{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#04BBBF">path</span>,<span style="color:#FCB13F">zone</span>}

#### SSL

SSL Labs grade.

> http.ssl.grade{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#04BBBF">path</span>,<span style="color:#FCB13F">zone</span>}

SSL validation until timestamp in second

> http.ssl.valid.until{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#04BBBF">path</span>,<span style="color:#FCB13F">zone</span>}

### DNS

#### Zone

DNS zone

> dns.zone{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#FCB13F">zone</span>}

#### Latency

DNS time to resolve hostname

> dns.lookup.latency{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#FCB13F">zone</span>}
