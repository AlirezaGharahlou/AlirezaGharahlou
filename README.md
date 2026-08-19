<div align="center">

```
┌──────────────────────────────────────────────────────────┐
│  alireza@backend:~$ whoami                                │
└──────────────────────────────────────────────────────────┘
```

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&pause=1200&color=39FF14&center=true&vCenter=true&width=750&height=50&lines=Alireza+Gharahlou" alt="name"/>

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=400&size=15&pause=1000&color=6E7681&center=true&vCenter=true&width=750&height=30&lines=Python+%2F+Django+%2F+DRF+Backend+Developer" alt="role"/>

<br/>

![Python](https://img.shields.io/badge/PYTHON-000?style=flat-square&labelColor=000&color=39FF14)
![Django](https://img.shields.io/badge/DJANGO-000?style=flat-square&labelColor=000&color=39FF14)
![PostgreSQL](https://img.shields.io/badge/POSTGRESQL-000?style=flat-square&labelColor=000&color=39FF14)
![Redis](https://img.shields.io/badge/REDIS-000?style=flat-square&labelColor=000&color=39FF14)
![Docker](https://img.shields.io/badge/DOCKER-000?style=flat-square&labelColor=000&color=39FF14)

</div>

<br/>

```diff
+ status: backend developer, currently shipping
+ location: building things that shouldn't break at 3am
+ mission: turn messy business requirements into boring, predictable systems
```

<br/>

## `$ cat about.md`

I build backend systems in **Python / Django / DRF** — mostly the kind that don't get to fail quietly. Order flows, payment logic, auth systems, and the integrations that sit between your database and someone else's API that goes down without warning.

My day-to-day lives in **service-layer architecture**: keeping the API layer dumb, pushing business logic somewhere testable, modeling databases so relationships actually reflect reality, and writing background workers that retry instead of panic.

I've spent real time inside **food-ordering and e-commerce style systems** — carts, orders, payments, product sync, vendor integrations, and the never-ending job of keeping two systems' data from quietly drifting apart.

<br/>

## `$ ls -la ~/stack`

<table>
<tr><th align="left">layer</th><th align="left">tech</th></tr>
<tr><td>lang</td><td><code>Python</code></td></tr>
<tr><td>backend</td><td><code>Django</code> · <code>Django REST Framework</code></td></tr>
<tr><td>data</td><td><code>PostgreSQL</code> · <code>Redis</code></td></tr>
<tr><td>auth</td><td><code>JWT</code> · <code>OTP</code> · <code>cookie-based auth</code></td></tr>
<tr><td>infra</td><td><code>Docker</code> · <code>Linux</code> · <code>Git</code></td></tr>
<tr><td>interfaces</td><td><code>REST APIs</code> · <code>third-party integrations</code></td></tr>
</table>

<br/>

## `$ cat services/backend.py`

```python
class BackendService:
    """
    What I actually spend my time doing, grouped by concern.
    """

    api_design = [
        "RESTful API development",
        "service-layer architecture",
        "business logic separation",
    ]

    data_layer = [
        "database modeling & relationships",
        "query optimization",
        "transactions",
        "caching strategy (Redis)",
    ]

    auth = [
        "JWT authentication",
        "OTP verification flows",
        "cookie-based sessions",
        "authorization systems",
    ]

    integrations = [
        "external API integrations",
        "vendor / third-party sync",
        "product & order synchronization",
        "background polling workers",
        "retry mechanisms for unreliable APIs",
        "data mapping: internal <-> external",
    ]

    domains = [
        "order management & cart systems",
        "payment flows",
        "food-ordering platforms",
    ]
```

<br/>

## `$ cat architecture.txt`

How I generally split a service — so the API layer stays replaceable and the business rules don't leak into it.

```
                    ┌────────────────────┐
   client  ───────▶ │   DRF API layer     │   thin: routing + serialization only
                    └─────────┬──────────┘
                              │
                    ┌─────────▼──────────┐
                    │   service layer     │   business logic, testable in isolation
                    └───┬────────────┬───┘
                        │            │
              ┌─────────▼───┐   ┌────▼──────────────┐
              │ PostgreSQL  │   │  Redis              │
              │ (source of  │   │  cache / queues     │
              │  truth)     │   └────┬────────────────┘
              └─────────────┘        │
                                ┌─────▼──────────────┐
                                │ background workers   │
                                │ polling + retry logic │
                                └─────┬──────────────┘
                                      │
                             ┌────────▼─────────┐
                             │ external / vendor  │
                             │ APIs (unreliable)  │
                             └────────────────────┘
```

```diff
+ API layer never touches business rules directly
+ external systems are treated as unreliable by default -> retries + idempotency
+ cache deliberately (hot paths only), not by default
+ data relationships modeled before queries get optimized
```

<br/>

## `$ tail -f current_focus.log`

```
[focus] sharpening service-layer patterns for cleaner, testable Django apps
[focus] building more resilient sync pipelines against vendor platforms
[focus] going deeper on Redis caching strategy under real load
[focus] tightening JWT / OTP auth flows for long-term maintainability
```

<br/>

## `$ ./run_stats.sh`

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=AlirezaGharahlou&show_icons=true&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=39FF14&icon_color=39FF14&text_color=8b949e&ring_color=39FF14"/>
<img height="165" src="https://github-readme-stats.vercel.app/api/top-langs/?username=AlirezaGharahlou&layout=compact&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=39FF14&text_color=8b949e"/>

<br/><br/>

<img src="https://github-readme-streak-stats.herokuapp.com/?user=AlirezaGharahlou&theme=github-dark-blue&hide_border=true&background=0d1117&stroke=39FF14&ring=39FF14&fire=39FF14&currStreakLabel=39FF14"/>

<br/><br/>

<img src="https://github-readme-activity-graph.vercel.app/graph?username=AlirezaGharahlou&theme=github-compact&hide_border=true&bg_color=0d1117&color=39FF14&line=39FF14&point=8b949e" width="95%"/>

</div>

<br/>

<!--
  Contribution snake — activates once the GitHub Action (snake.yml) has run at least once.
  Broken image before that is expected, not a bug in the README.
-->
<div align="center">

![snake](https://raw.githubusercontent.com/AlirezaGharahlou/AlirezaGharahlou/output/github-contribution-grid-snake-dark.svg)

</div>

<br/>

## `$ cat pinned_repos.md`

> GitHub Actions can't invent your projects for you — pin your best repos from your profile page (`Customize your pins`), then swap the placeholders below with the real repo names.

<div align="center">

<!-- swap REPO-NAME-1 / REPO-NAME-2 for your actual repository names -->
<a href="https://github.com/AlirezaGharahlou/REPO-NAME-1">
  <img height="150" src="https://github-readme-stats.vercel.app/api/pin/?username=AlirezaGharahlou&repo=REPO-NAME-1&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=39FF14&text_color=8b949e"/>
</a>
<a href="https://github.com/AlirezaGharahlou/REPO-NAME-2">
  <img height="150" src="https://github-readme-stats.vercel.app/api/pin/?username=AlirezaGharahlou&repo=REPO-NAME-2&theme=github_dark&hide_border=true&bg_color=0d1117&title_color=39FF14&text_color=8b949e"/>
</a>

</div>

<br/>

## `$ cat philosophy.md`

```
> reliability beats cleverness
  a boring retry mechanism that never fails beats a clever one that fails silently

> data consistency is not optional
  sync bugs stay quiet until they don't — design against that from day one

> thin API, thick service layer
  views and serializers should be too dumb to have bugs worth writing tests for
```

<br/>

## `$ cat contact.sh`

```bash
#!/bin/bash
github="https://github.com/AlirezaGharahlou"
# linkedin=""   <- add your LinkedIn URL here
# email=""      <- add your email here
# telegram=""   <- add your Telegram here

echo "reach me on GitHub, always open to backend / Python conversations."
```

<div align="center">

[![GitHub](https://img.shields.io/badge/GITHUB-000?style=for-the-badge&labelColor=000&color=39FF14&logo=github&logoColor=39FF14)](https://github.com/AlirezaGharahlou)

</div>

<br/>

<div align="center">

```
alireza@backend:~$ process exited with code 0
```

<sub>thanks for reading the source instead of just the summary.</sub>

</div>
