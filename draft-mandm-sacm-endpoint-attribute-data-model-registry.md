---
title: SACM Endpoint Attribute Data Model Registry
abbrev: SACM EADM Registry
docname: draft-mandm-sacm-endpoint-attribute-data-model-registry-latest
stand_alone: true
ipr: trust200902
area: Security
wg: SACM Working Group
kw: Internet-Draft
cat: std
coding: us-ascii
pi:
  toc: yes
  sortrefs: yes
  symrefs: yes

author:
- ins: A. Montville
  name: Adam W. Montville
  org: Center for Internet Security
  abbrev: CIS
  email: adam.w.montville@gmail.com
  street: 31 Tech Valley Drive
  code: '12061'
  city: East Greenbush
  region: NY
  country: USA
- ins: B. Munyan
  name: Bill Munyan
  org: Center for Internet Security
  abbrev: CIS
  email: bill.munyan.ietf@gmail.com
  street: 31 Tech Valley Drive
  code: '12061'
  city: East Greenbush
  region: NY
  country: USA

normative:
  mandm-sacm-collection-model:
  mandm-sacm-architecture-redux:
  I-D.mandm-sacm-architecture:


informative:



--- abstract

This memo describes a an interface to registries used to store endpoint attribute data models. These data models are used for the purpose of automated endpoint assessment.

WORKING GROUP: The source for this draft is maintained in GitHub.  Suggested changes should be submitted as pull requests at https://github.com/adammontville/draft-mandm-sacm-endpoint-attribute-data-model-registry.  Instructions are on that page as well.

--- middle


# Introduction

Security automation assessments (i.e. vulnerability assessment, configuration assessment, etc.) often require enumerations of endpoint attributes to be known before such assessments can take place. As technologies evolve and emerge, enumerations may change and new enumerations come into existence. As such changes to the set of enumerations happen frequently. A problem yet to be solved in security automation is the ability for enterprises to quickly, even dynamically, acquire (or potentially define) enumerations of endpoint attributes and make those enumerations available to the security automation tools operating in their enterprise.

## Scope of Solution

The scope of this solution is constrained to the repository interface, and specifically avoids details about the data models stored in the repository. This is because data models may vary, depending on attribute collection needs. Coarsely, network devices are likely to have models represented using YANG, whereas traditional devices may be represented using OVAL.


# Terms and Definitions

TBD

# Repository Interface

An implementation of a data model repository MUST support the following operations:

* List data models
* Get data model X
* Add data model
* Update data model
* Remove data model

Authorizations MUST be considered in an implementation. Listing and getting data models SHOULD be open, but MAY be constrained to authorized entities. Adding, updating, and removing data models SHOULD be restricted to authorized entities only, but MAY be opened to the world. In other words, this document does not take a strong stance on what should or should not be authorized for a given repository.

# Repository Data Model Metadata

In order for a repository to be queryable, a certain structure of metadata about the data models needs to be described.

* Name
* Version
* Endpoint applicability
* Date created
* Date last modified
* Author (individual or organization)
* Others???

#  IANA Considerations

This draft may end up defining one or more IANA tables.

#  Security Considerations

TBD

#  Acknowledgements

TBD

#  Change Log

TBD


# Contributors
TBD

--- back

# The Attic

TBD
