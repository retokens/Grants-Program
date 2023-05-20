# Know Your Real-estate Asset

* **Status:** Open (anyone is allowed to apply) / Closed (invited respondents only) / Implemented (finished)
* **Proposer:** REtokens.com
* **Your Project(s):** [optional]: Link(s)
* **Projects you think this work could be useful for** [optional]: Polymath Capital Platform
* **Teams/People that could deliver the RFP** [optional]: Link(s)

## Project Description :page_facing_up: 

//Please describe exactly why you are proposing this RFP. 

//Make sure to point out why it’s potentially useful for your project or other projects in the ecosystem.  

**Introduction**
In a business and investment world of rapid digitization, decentralization and frequent lack of regulation and oversight, fraud is a sophisticated, enduring and intrusive threat.

A single act of investment fraud perpetrated on an investor on the
Polymath Capital Platform (PCP) could have long-term, 
devastating consequences for the PCP and it's ability to attract asset issuers and investors.

The purpose of the Know Your Real-estate Asset project is to reduce the potential of fraud 
as much as possible in order to protect the integrity of the PCP and the interests of its investors in RE STOs.

Note: On one hand, we have limited the scope of this project to fraud prevention for 
real-estate backed STOs (RE STOs) only.
On the other hand, we presume that the approach
taken here will apply equally well to non-RE STOs, with some adjustments.
Our thinking is to focus on the single problem of RE STO fraud prevention and achieve it,
rather than the universal problem of fraud prevention, and later apply it to other types of STOs.

While real estate fraud in the physical or digital world cannot be prevented entirely, 
it is REtokens' position 
that the threat of fraud can be greatly reduced by increasing the veracity of RE STOs documentation
traditional documentation made available via the PCP.

And while there are different types of RE STO fraud a perpetrator could commit, 
the scope of this project is limited to preventing issuance of a RE STO:

- with non-existent backing property
- with a backing property which is not 'owned' by the issuer

**Objectives**

The objectives of this project are:

- to define which documents best serve guaranteeing RE STO veracity.

- to make it simple and cost-effective for issuers to demonstrate RE STO veracity.

- to ensure potential investors can perform due diligence on the veracity of the backing property easily and with confidence

- to define and implement a technical process for storing or referencing documentation from the PCP in a manner which guarantees documentation integrity via hashing and issuer non-repudiation via digital signature.

**Impact**

The impact of this project will be to make it easier for potential investors to recognize RE STOs which are fraudulent as related to their existence or ownership.

The ultimate effect will be to discourage and prevent issuance of fraudulent RE STOs in the first place.

**Expected Outcomes**

An outcome of this project is enabling 
potential investors to access conclusive RE STO 
due diligence documentation fast and with confidence 
directly or indirectly from the blockchain. 
This can accelerate word-of-mouth promotion which will drive network effect adoption.

This storage, as well, of other due diligence 
documents and/or references on-chain will greatly 
dematerialize the due diligence process in other areas, 
such as valuation.

## Deliverables :nut_and_bolt:
The PCP in its current form should be able to support the addition of the due diligence 
document(s) listed below.

There are additional steps that could be made but this would require discussion 
and cost/benefit analysis.

Therefore, unless further analysis is needed based on the remainder of this section, 
there are no concrete deliverables for this project.

***Title Report***

The simplest most effective way for an issuer to prove ownership 
and existence of a RE STO backing property is to 
property's Title Report ([see](https://www.fortunebuilders.com/what-is-title-report/))

A Title Report checks the important boxes related to preventing property fraud, providing practically
all the necessary due diligence related to the issues of property existence and ownership:

* **Legal Description** 
* **Parcel Number**
* **Owner**
* **Lien Holders**
* **Encumbrances**
* **Easements**
* **Title Claims due to Mortgage or Debt**

***Title Report as Asset Document Reference***

There are two ways to make the Title Report available to potential investors.

The first is as an Asset Document, as seen here ([see](./AssetDocumentExample.png)).

This is the simplest approach and can be applied to any type of documentation which 
improves the veracity property documentation.

The issuer would add the Title Report reference via a signed transaction which would 
impose non-repudiation on the issuer which would give them pause if their intention was fraud.

The potential investor would need to click the 'document' link to view the 
real Title Report in a browser as is done now or, alternatively, in a custom viewer.

***Title Report as On-chain as part of the Asset***

The second way is to the store the Title Report On-chain as part of the RE STO Asset. 

The necessity of this is questionable and would add complexity and cost.

**On-Chain Versioning**

A closer Cost/Benefit analysis would need to be done, but one obvious benefit would be
that the Asset would have a 'content-management' or 'source-control' versioning of the 
due diligence documents associated with it which would make fraud easy to prove and, thereby, 
give more pause to a bad actor.

Versioning is difficult with off-chain references, unless the documents 
were persisted in an immutable store which seems like a difficult requirement to enforce without
supporting storage infrastructure or application process support. 
But, in light of the consequences of fraud, this may be an approach to consider as the infrastructure 
or process support could be lightweight.

***Document Hash***
Regardless of whether the documentation is stored as
a reference or on-chain. 
The document's cryptographic hash must be persisted as well as it is the Hash
which gives the potential investor the guaranteed of document integrity. Without the hash, 
the document could be swapped out for another or modified.

Generating a hash for a document might be an area where work needs to be done since the average 
issuer would probably not know how to do that.

***Digital Signature***
When a document is 'added' to the Asset (as reference or on-chain data) and a hash is included,
the issuer signs the transaction. At that moment, the issuer is effectively 
making a digitally signed claim about the existence and integrity of 
the document which cannot be repudiated.

Making false claims and/or submitting falsified or misleading documentation 
about a digital security and not being able to repudiate the act should 
be a powerful disincentive to bad actors hoping to commit fraud.

* **Total Estimated Duration:** TBD
* **Full-time equivalent (FTE):**  TBD 

### Milestones
There are no milestones at this time.

Discussion regarding this proposal need to take place before milestones are declared.
