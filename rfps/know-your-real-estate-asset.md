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
as much as possible in order to protect the integrity of the PCP and the
interests of its investors in Real-estate backed Security Tokens (RE STOs).

Note: On one hand, we have limited the scope of this project to fraud prevention for 
RE STOs only.
On the other hand, we presume that the approach
taken here will apply equally well to non-RE STOs, with some adjustments.
Our thinking is to focus on the single problem of RE STO fraud prevention and achieve it,
rather than the universal problem of fraud prevention. Later, we can apply a similar approach 
to other types of STOs.


And while there are different types of RE STO fraud a perpetrator could commit, 
the scope of this project is limited to preventing issuance of a RE STO:

- with non-existent backing property
- with a backing property which is not 'owned' by the issuer


**Objectives**

While real estate fraud in the physical or digital world cannot be prevented entirely,
it is REtokens' position
that the threat of fraud can be greatly reduced
by increasing the veracity of RE STOs documentation
made available via the PCP.

Therefore, the objectives of this project are:

- to define which documents best serve guaranteeing RE STO veracity.

- to make it simple and cost-effective for issuers to demonstrate veracity of RE STO documentation
- to ensure potential investors can easily and confidently perform 
due diligence on the veracity of the backing property

- to define and implement a technical process for 
storing or referencing documentation from the PCP in a manner which guarantees documentation integrity via hashing and issuer non-repudiation via digital signature.

**Impact**

The impact of this project will be to make it easier for 
potential investors to recognize RE STOs 
which are fraudulent as related to their existence or ownership.

The ultimate effect will be to discourage, if not prevent, issuance of 
fraudulent RE STOs in the first place.

**Expected Outcomes**

An outcome of this project is to enable 
potential investors to access conclusive RE STO 
due diligence documentation easily and with confidence, either 
directly on the blockchain or indirectly via 
document URLs to centralized or decentralized storage. 

Ease and confidence can accelerate word-of-mouth promotion 
which will drive network effect adoption of the PCP.

Consequently, readily accessible, high veracity due diligence documentation via the PCP 
will greatly dematerialize the due diligence process in other areas as well, 
such as determining RE STO valuation.

## Deliverables :nut_and_bolt:
The PCP in its current form should be able to support the addition of the due diligence 
document(s) listed below.

There are additional steps that could be taken but this would require a pros and cons
discussion with the PCP team as well as a cost/benefit analysis.

Some ideas are:

 - storage on the blockchain, linked to the RE STO
 - PCP extension application to help issuers publish documentation to Polymesh or external
storage
 - PCP tools or utilities to enable automatic inclusion of
document hashes and digital signatures to ensure document integrity and issuer non-repudiation
 - taxonomy definition for RE STOs documentation sets
(as a basis for other STO-type documentation sets)

Therefore, unless further analysis is needed, and based on the remainder of this section, 
there are no concrete deliverables for this project as it is believed that the PCP
as is can support the 'attachment' of documentation the issued RE STO.

***Title Report***

RETokens believes that the simplest, most effective way for an issuer to prove existence and
ownership of an RE STO backing property is to attach to the RE STO the 
property's Title Report ([see](https://www.fortunebuilders.com/what-is-title-report/))

A Title Report checks 'all the important boxes' related to preventing property fraud
by providing practically
all the necessary due diligence related to proving the property existence and issuer ownership:

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
improves the veracity of property documentation.

The issuer would add the **Title Report** reference via a signed transaction which would 
impose non-repudiation on the issuer, 
a fact which would give them pause if their intention were fraud.

The potential investor would need to click the 'document' link to view the 
real **Title Report** in a browser as is done now or, alternatively, in a custom viewer.

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
be a powerful deterrent to bad actors hoping to commit fraud.

***Folder Structures and Templates***
Including Folder Structures in the PCP could improve Asset documentation organization 
as compared to the flat structure in place today.

For example, a **Due Diligence** folder would allow issuers to put documentation into a single location and 
give potential investors a single location to look for due diligence information.

Folder templates **per Asset Type** could be defined and applied during Asset initialization, giving 
issuers and potential investors visual triggers to what should be included and where to find it.

* **Total Estimated Duration:** TBD
* **Full-time equivalent (FTE):**  TBD 

### Milestones
There are no milestones at this time.

Discussion regarding this proposal need to take place before milestones are declared.
