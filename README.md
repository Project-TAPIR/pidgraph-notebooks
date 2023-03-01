# pidgraph-notebooks

[![DOI](https://zenodo.org/badge/447263093.svg)](https://zenodo.org/badge/latestdoi/447263093)
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Project-TAPIR/pidgraph-notebooks/main)

A collection of Jupyter notebooks with examples of querying different PID providers like [ORCID](https://orcid.org/), [ROR](https://ror.readme.io/), [Crossref](https://www.crossref.org/) and PID graphs like the [FREYA PID Graph](https://blog.datacite.org/powering-the-pid-graph/), [OpenAlex](https://openalex.org/about) and [OpenAIRE](https://www.openaire.eu/) for connected objects. 

Currently included connections:
* organization-organization
  * input: ROR
  * output: hierarchy of sub-organizations starting at given organization, each identified by their ROR
  * data sources: ROR
* organization-people
  * input: ROR
  * output: list of people affiliated with the organization, each identified by their ORCID iD
  * data sources: FREYA PID Graph, OpenAlex, ORCID
* organization-works
  * inout: ROR
  * output: list of works affiliated with an organization, each identified by their DOI 
  * data sources: Crossref, OpenAlex 
* person-works
  * input: ORCID
  * output: list of works authored/created by the person, each identified by their DOI
  * data sources: Crossref, FREYA PID Graph, OpenAlex, ORCID, OpenAIRE
* work-projects
  * input: DOI
  * output: list of projects the work was produced in, each identified by their OpenAIRE project ID
  * data sources: OpenAIRE
* Search for experts
  * input: ORCID ID, OpenAlex Concept
  * output: ORCiD ID with the respective Concepts and there concept score
  * data source: OpenAlex
* Search for funder informations
  * input: ROR, ORCID, DOI
  * output: list of DOIs and there funder informations
  * data source: Crossref

Please navigate into the respective folder to see the list of available notebooks. 

### Run notebooks
While GitHub renders Jupyter notebooks as static HTML files (not executable), 
you can use this link to launch the notebooks on Binder where you can execute and modify them:
[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/Project-TAPIR/pidgraph-notebooks/main)

[![Screenshot Binder](Binder.png)](https://mybinder.org/v2/gh/Project-TAPIR/pidgraph-notebooks/main)

----------------------------

### Background
In the joint project [TAPIR](https://projects.tib.eu/tapir/en/) (Partially Automated Persistent Identifier-based Reporting), partially automated procedures for research reporting are being tested in the context of university and non-university research. To this end, the question is being investigated : 

To what extent can the necessary data aggregation be carried out on the basis of openly available research information using persistent identifiers?

*More information in our blog post "[Project TAPIR: Harvesting the power of PIDs](https://blogs.tib.eu/wp/tib/2022/03/01/project-tapir-harvesting-the-power-of-pids/)"*
