## CircleCI

---

## Hva?

SaaS - løsning for automatisk bygging og deploy (CI/CD)

---

## Hvordan?
* hvert repo har en `.circleci` mappe med en `config.yml`
* CircleCI bygger på github/bitbucket hooks
* "Byggene" kjøres i docker-containere

---

## Rettigheter

Styres av Bitbucket, Github osv.
For å styre spesifikke ting som `Project settings` må du være admin eller project owner.

---

## Context

Felles parametere legges i en context.
F.eks nexus/jfrog-innlogging.

---
## CircleCI CLI

* Validere config lokalt
* Kjøre jobber lokalt. (workflows og cache ikke støttet)

----

## Rerun with SSH

Logg inn i container som kjører jobben.

---


## Sikkerheten?

Ikke gjør
```
echo ${GCLOUD_SERVICE_KEY}
```
Bygglogg er åpne default. Vurder å stenge.

---




## Pull Requester

Vi kan ikke bygge (kjøre tester) pull requester så lenge vi trenger secrets for å kjøre testene.

---

## Varsling til Babylon

CircleCI sender tilsvarende JSON-format ved ferdig bygg som Jenkins.
Scriptet ligger i https://circleci.com/gh/entur/circleci-toolbox-image/

---

## Downstream triggering


---

## Personlige API-token

Personlig API-token for å trigge workflows med Curl


---

## Ulemper
* se hvor noe blir trigget fra

---

### Links
Presentasjonens URL:
https://gitpitch.com/csolem/gitputch-entur-circleci#/

Presentasjonen på github
https://github.com/csolem/gitputch-entur-circleci#/
