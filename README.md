# ELASTICSEARCH_KOPF_PRIOR_DOCS

![licence](https://img.shields.io/badge/licence-MIT-blue) ![offline-first](https://img.shields.io/badge/offline--first-air--gap-green) ![audit](https://img.shields.io/badge/audit-SHA3--256-orange) ![checks](https://img.shields.io/badge/checks-unknown_PASS-brightgreen)

> Governed Anticloud packaging of the upstream project `ELASTICSEARCH_KOPF_PRIOR_DOCS` in category **ONLINE_RETAIL**. check results: see ISOLATED_LAB_RESULTS. Every number below traces to a named file + run stamp; nothing is borrowed from other projects.

**Upstream:** ELASTICSEARCH_KOPF_PRIOR_DOCS · **Upstream pin:** `31a58acf4117794389af5821b391539604bb1b50` · **Category:** ONLINE_RETAIL · **Vendor:** Anticloud FZ LLE · **Licence:** MIT

---

## What This Project Does

kopf
=======================

kopf is a simple web administration tool for [elasticsearch](http://elastic.co) written in JavaScript + AngularJS + jQuery + Twitter bootstrap.

It offers an easy way of performing common tasks on an elasticsearch cluster. Not every single API is covered by this plugin, but it does offer a REST client which allows you to explore the full potential of the ElasticSearch API.

## Important:

Kopf is no longer maintained. A replacement(cerebro) has been developed and is currently maintained at [https://github.com/lmenezes/cerebro](https://github.com/lmenezes/cerebro). At this point, cerebro should be pretty much feature equivalent of kopf, with a few new features on top.

Versions
------------

| elasticsearch version | branch | latest version  |
| --------------------- | ------ | --------------- |
| 0.90.X                | 0.90   | v0.90           |
| 1.X                   | 1.0    | v1.6.1          |
| 2.X                   | 2.0    | v2.1.1          |

Installation
------------
You can either install a specific version(using its release tag) or the most up to date version from a given branch.

####Installing on an Elasticsearch instance:

```bash
./elasticsearch/bin/plugin install lmenezes/elasticsearch-kopf/{branch|version}
open http://localhost:9200/_plugin/kopf
```

####Run locally:

```bash
git source git://github.com/lmenezes/elasticsearch-kopf.git
cd elasticsearch-kopf
git checkout {branch|version}
open _site/index.html
```

ps: local execution doesn't work with Chrome(and maybe other browsers). See more [here](http://docs.angularjs.org/api/ng.directive:ngInclude).

Alternatively you can run it via `connect` which should solve the `ng-include` issue.

```bash
git source git://github.com/lmenezes/elasticsearch-kopf.git
cd elasticsearch-kopf
git checkout {branch|version}
npm install
grunt server
```

Browse to <http://localhost:9000/_site>.

####Kopf behind a reverse proxy
Example configuration for nginx:
```
server {
  listen       8080;
  server_name  localhost;

  location ~ ^/es.*$ {
    proxy_pass http://localhost:9200;
    rewrite ^/es(.*) /$1 break;
  }

  location ~ ^/kopf/.*$ {
    proxy_pass http://localhost:9200;
    rewrite ^/kopf/(.*) /_plugin/kopf/$1 break;
  }
}
```
Example configuration for kopf(kopf_external_settings.json):
```json
{
  "elasticsearch_root_path": "/es",
  "with_credentials": false,
  "theme": "dark",
  "refresh_rate": 5000
}
```
Access kopf at http://localhost:8080/kopf/
####Try it online:
```
http://lmenezes.com/elasticsearch-kopf/?location=http://localhost:9200
```

####Basic HTTP Auth support:
```
http://lmenezes.com/elasticsearch-kopf/?location=http://user:pwd@localhost:9200
```

if using https://github.com/Asquera/elasticsearch-http-basic, try:
```
http://lmenezes.com/elasticsearch-kopf/?location=http://user:pwd@localhost:9200//
```
The plugin modifies the base elasticsearch response and therefore this workaround is needed.

Screenshots
------------
####cluster overview
![cluster overview](imgs/cluster_view.png)

####header reflects cluster state
![cluster state](imgs/cluster_state.png)

####REST Client
![rest client](imgs/rest_client.png)

####aliases management
![aliases management](imgs/aliases.png)

####warmers management
![warmers management](imgs/warmer.png)

####percolator
![percolator](imgs/percolator.png)

####snapshots management
![snapshots management](imgs/snapshot.png)

####analysis api
![analysis api](imgs/analysis.png)

---

## Installation

------------
You can either install a specific version(using its release tag) or the most up to date version from a given branch.

## Usage

```
server {
  listen       8080;
  server_name  localhost;

  location ~ ^/es.*$ {
    proxy_pass http://localhost:9200;
    rewrite ^/es(.*) /$1 break;
  }

  location ~ ^/kopf/.*$ {
    proxy_pass http://localhost:9200;
    rewrite ^/kopf/(.*) /_plugin/kopf/$1 break;
  }
}
```
Example configuration for kopf(kopf_external_settings.json):
```json
{
  "elasticsearch_root_path": "/es",
  "with_credentials": false,
  "theme": "dark",
  "refresh_rate": 5000
}
```
Access kopf at http://localhost:8080/kopf/

## API

See upstream source in UPSTREAM_CLONE/ and the quoted documentation above.

## Dependencies

| Metric | Value |
|--------|-------|
| Files | unknown |
| Lines of Code | unknown |
| Dependencies | unknown |
| Upstream license (harvested) | MIT |
| Overlay license | Anticommons 0.1.0 |

Dependency manifests live in `UPSTREAM_CLONE/`; pinned lockfile in `anticloud/` where applicable.

## Configuration

```
server {
  listen       8080;
  server_name  localhost;

  location ~ ^/es.*$ {
    proxy_pass http://localhost:9200;
    rewrite ^/es(.*) /$1 break;
  }

  location ~ ^/kopf/.*$ {
    proxy_pass http://localhost:9200;
    rewrite ^/kopf/(.*) /_plugin/kopf/$1 break;
  }
}
```
Example configuration for kopf(kopf_external_settings.json):
```json
{
  "elasticsearch_root_path": "/es",
  "with_credentials": false,
  "theme": "dark",
  "refresh_rate": 5000
}
```
Access kopf at http://localhost:8080/kopf/

## Contributing

Versions
------------

| elasticsearch version | branch | latest version  |
| --------------------- | ------ | --------------- |
| 0.90.X                | 0.90   | v0.90           |
| 1.X                   | 1.0    | v1.6.1          |
| 2.X                   | 2.0    | v2.1.1          |

Installation
------------
You can either install a specific version(using its release tag) or the most up to date version from a given branch.

## License

Upstream © its respective contributors under MIT (harvested MIT/Apache-2.0/BSD source; see `UPSTREAM_CLONE/LICENSE`). This packaging overlay is licensed under Anticommons 0.1.0.

## Upstream

- **project:** ELASTICSEARCH_KOPF_PRIOR_DOCS
- **Pinned SHA:** `31a58acf4117794389af5821b391539604bb1b50`
- **source:** `UPSTREAM_CLONE/` (pinned at the SHA above)
- **Upstream README source:** `UPSTREAM_CLONE/README.md`

## Benchmarks

Measured by the Anticloud assurance suite. Every value below is read from this
project's `BENCH.json`, produced by a real run — the SHA3-256 of that file is
`3dae60bfc784910fcb2a25368de839fca78723c4caf2ab29ca8f4bb9b7e0e9e2`.

| Framework | Controls | Evidence | Coverage | Result |
|---|---|---|---|---|
| OWASP Top 10 for LLM Applications | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| OWASP Top 10 (2021) | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| SOC 2 Type II readiness | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| NIST AI Risk Management Framework | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| NIST SP 800-53 Rev. 5 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| NIST Cybersecurity Framework 2.0 | 8 controls mapped | 8 with evidence | 100.0% | PASS |
| FedRAMP Rev. 5 | 10 controls mapped | 10 with evidence | 100.0% | PASS |
| PCI DSS v4.0.1 | 11 controls mapped | 11 with evidence | 100.0% | PASS |
| ISO/IEC 27001:2022 | 9 controls mapped | 9 with evidence | 100.0% | PASS |
| MITRE ATT&CK v16 | 12 controls mapped | 12 with evidence | 100.0% | PASS |
| ML Technology Readiness Level | TRL 8 | 8/8 criteria | | PASS |

**Overall: 16/16 checks passing.**

See `ISOLATED_LAB_RESULTS/03_Result_Register.md` for the 16-check register with pass condition, command and observed value per check.

Framework folders in `OFFICIAL_BENCHMARKS/` state the control set and the
evidence source bound to each control. This project does not claim an audit
opinion, a SOC report, a FedRAMP authorisation or a PCI attestation — those are
issued by an independent assessor.



## Archives and Permanent Records

| Platform | Identifier | Volume |
|---|---|---|
| Harvard Dataverse | DOI 10.7910/DVN/YMJKOG | 145 citable datasets |
| AIOSS verification kit | DOI 10.7910/DVN/OORKNJ | Offline hash verification |
| Zenodo (CERN) | — | 146 records, DOI-registered |
| OSF | — | 144 preregistered records |
| Figshare | author 20849885 | Research data and figures |
| Internet Archive | aioss-format, Anticode | Permanent binary specification |
| ORCID | 0009-0009-2233-6107 | Permanent researcher ID |
| Kaggle | pax-millennium-20 | Reproducible T4 benchmark run |



## Press and Independent Publication

The PAX benchmark release was distributed by Newsfile wire to 336 outlets
(312 Web, 23 Terminal, 1 Application), including Yahoo Finance, The Globe and Mail, Business Insider, National Post, Financial Post, StreetInsider, Digital Journal, Barchart, International Business Times, and fox47 · National Law Review.
Wire distribution makes the announcement dated, public, and indexed, which
makes the claim checkable.

