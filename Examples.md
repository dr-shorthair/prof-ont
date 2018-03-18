# Examples

## Implementation: Energy Use Data Model
The [Energy Use Data Model (EUDM)](https://eudm.csiro.au) project is building a platform for discovering data, research and reports from across the Australian energy sector. One part of the project work is to create a metadata model for EUDM datasets which are about energy, energy consumption, production and related information. In order to make such a model that is both interoperable with generic dataset metadata models and also able to cater for the EUDM projects's specific requirements, a profile of the well-known [W3C](https://www.w3.org)'s [Data Catalog Vocabulary (DCAT)](https://www.w3.org/TR/vocab-dcat/) will be used.

### EUDM restrictions on DCAT 1.0
* DCAT allows for `Dataset` keywords to be indicated with `dcat:keyword`
  * `EUDM Datasets` **MUST** have at least one keyword from each of the following vocabularies:
    * EUDM Major Categories vocabulary
    * *more to come...*

* DCAT allows for a `Dataset`'s `Distribution` to have a license indicated with `dct:license`
  * `EUDM Datasets`, when viewed in DCAT 1.0 compatability mode, must have at least one `Distribution` and each `Distribution` must have a `dct:LicenseDocument`s indicated
  * the `dct:LicenseDocument`s indicated must come from the [AGISO](http://linked.data.gov.au/agiso) Licenses Register
  
### EUDM restrictions on DCAT 1.1
DCAT 1.1 extends DCAT 1.0's handling of licenses by allowing a super property of `dct:license`, `odrl:hasPolicy` to indicate an object other than a `dct:LicenseDocument`.

* `EUDM Datasets`, when viewed natively (i.e. no compatability mode) must have at least one `Distribution` and each `Distribution` must have an `agr:Agreements` class object (subclass of `odrl:Policy`) indicated using `odrl:hasPolicy`
 * additionally, the `agr:Agreements` object must come from the controlled Agreements Register maintained by the [Australian Government Linked Data Working Group](http://linked.data.gov.au)
* *more to come...*
