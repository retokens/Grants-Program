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

There are additional development areas that could be taken but this would require discussions
with the PCP team including pros and cons assessment and cost/benefit analysis.

Potential development areas include:

 - a PCP tool, utility, UI extension or API to
   - help issuers publish documentation to
     centralized off-chain storage service or direct on the blockchain
   - generate a hash or validate a provided
hash when a document URL is added to the RE STO's documentation set (the Polkadot.js API has
   a limitation in that it 'accepts'
a 'contentHash' argument but does not validate it
(as can be seen in polymesh-sdk-examples/src/examples/createToken.ts)
   - Include a digital signature to each document 
   to impose a more visible enforcement of issuer non-repudiation
 - define a PCP-visible taxonomy for RE STOs documentation sets (later, this approach
could be adapted to other STO-type documentation sets)
 - custom document viewer which would include a 'hash validation' step. The viewer could
make document integrity or corruption obvious to anyone looking at the document.
 
If none of the above development areas are deemed necessary, 
then this proposal includes no specific concrete deliverables as it is currently
possible to attach document references to RE STOs.

***Title Report***

RETokens believes that the simplest, most effective way for an issuer to prove existence and
ownership of an RE STO backing property is to attach a reference to the 
property's Title Report to the RE STO ([see](https://www.fortunebuilders.com/what-is-title-report/))

This is because the Title Report checks 'all the important boxes' relevant 
to preventing property fraud
by providing practically
all the necessary due diligence information 
to proving the property existence, the issuer ownership and title quality:

* **Legal Description** 
* **Parcel Number**
* **Owner**
* **Lien Holders**
* **Encumbrances**
* **Easements**
* **Title Claims due to Mortgage or Debt**

***Title Report as Document Reference***

There are two ways to make the Title Report available to potential investors.

The first is to attach a reference to an externally **Title Reportt** to the RE STO, 
as seen in this screenshot ([see](./AssetDocumentExample.png)). Presumably, this is done 
via the Polkadot.js API, but as is mentioned above, there is a limitation when using this API 
in that it neither generates a document hash nor validates the hash provided to the API.

This is the simplest approach and can be applied to any type of documentation which 
improves the veracity of property documentation.

The issuer would add the **Title Report** reference via a signed transaction. 
The signed transaction
would create a de facto digital signature for the referenced document submission and, thereby, 
impose non-repudiation on the issuer: non-repudiation of a fraudulent document to a RE STO wouild 
give serious pause to any potential fraudster.

For a potential investor to view the document, 
they would click the 'document' link to view the 
referenced **Title Report** in a browser as is done now or, alternatively, in a custom viewer which could
provide a hash-based integrity check.

***Title Report Stored (and Versioned) On-chain***

The second way is to the store the Title Report On-chain and linked to the RE STO. 

The desirability of this approach should be questioned because it would add bloat, 
complexity and cost to the Polymesh blockchain.

However, if on-chain document storage were limited to only the **Title Report** 
there is the downstream benefit of **On-Chain Versioning** that may be worth the cost.

On-chain document storage provides an out-of-the-box 
'content-management' type of audit trail, making the act of submitting a fraudulent 
**Title Report** more threatening to a fraudster due to its on-chain, immutable provability.

In contrast, provability is difficult to achieve with an off-chain 
**Title Report** reference, unless it was
persisted in an immutable store. Making immutable storage seems like a difficult 
requirement to enforce without
supporting storage infrastructure or application process support. 
Therefore, in light of value of preventing fraud, on-chain storage or off-chain immutable storage
may be an approaches to consider as the infrastructure or 
process support could be relatively lightweight to create or already existing.

***Taxonomy Folder Structures and Templates***
as compared to the flat file structure in place today,
including Taxonomy Folder Structures in the PCP could improve RE STO documentation organization.

For example, a **Due Diligence** folder would allow issuers to put 
due diligence documentation into a single location. This kind of organization would 
give potential investors a single location to look for due diligence information.

Folder templates **per Asset Type** could be defined and 
applied during Asset initialization/issuance, giving 
issuers and potential investors visual triggers to what should be included and where to find it.

* **Total Estimated Duration:** TBD
* **Full-time equivalent (FTE):**  TBD 

### Milestones
There are no milestones at this time.

Discussion regarding this proposal need to take place before milestones are declared.
