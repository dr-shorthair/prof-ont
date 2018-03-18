# Examples

## Implementation: Energy Use Data Model
The [Energy Use Data Model (EUDM)](https://eudm.csiro.au) project is building a platform for discovering data, research and reports from across the Australian energy sector. One part of the project work is to create a metadata model for EUDM datasets which are about energy, energy consumption, production and related information. In order to make such a model that is both interoperable with generic dataset metadata models and also able to cater for the EUDM projects's specific requirements, a profile of the well-known [W3C](https://www.w3.org)'s [Data Catalog Vocabulary (DCAT)](https://www.w3.org/TR/vocab-dcat/) will be used.

### EUDM restrictions on DCAT
* DCAT allows for `Dataset` keywords to be indicated with `dcat:keyword`
  * `EUDM Datasets` **MUST** have at least one keyword from each of the following vocabularies:
    * EUDM Major Categories vocabulary
    * *more to come...*

* DCAT allows for a `Dataset`'s `Distribution` to have a license indicated with `dct:license`
  * `EUDM Datasets` must have at least one `Distribution` and each `Distribution` must have a license indicated
  * the licenses indicated must come from the [AGISO](http://linked.data.gov.au/agiso) Licenses Register
