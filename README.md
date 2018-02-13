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

HTTP Response status (200, 500, …)

**Format:** http.response.status{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#04BBBF">path</span>,<span style="color:#FCB13F">zone</span>}

#### Response Time

HTTP Response time in ms

**Format:** http.response.time{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#04BBBF">path</span>,<span style="color:#FCB13F">zone</span>}

#### SSL Grade

SSL Labs grade

**Format:** http.ssl.grade{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#04BBBF">path</span>,<span style="color:#FCB13F">zone</span>}

### DNS

#### Zone

DNS zone

**Format:** dns.zone{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#FCB13F">zone</span>}

#### Latency

DNS time to resolve hostname

**Format:** dns.lookup.latency{<span style="color:#C2024F">domain</span>,<span style="color:#741b47">host</span>,<span style="color:#FCB13F">zone</span>}
