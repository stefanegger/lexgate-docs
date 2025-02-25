---
title: "Create Utility Bills"
date: 2020-02-03T13:00:00
lastmod: 2020-02-03T13:00:00
weight: 301
draft: false
keywords: ["utility", "bill", "create", "costs", "items", "contract", "contracts", "period", "periods", "billing"]
---

In Lexgate you can create periodic Utility Bills with a few steps. It's required that your Project has it's Cost Centres set up. How to set up Cost Centres is described [here]({{<relref "/project-creation/accounting-structure">}}).

### Billing Period
A Billing Period defines the period which should be used for an Utility Bill. You can create one in {{<lga-nav text="Billing Period">}}.

As soon as a Billing Period is used for an Utility Bill, it can't be changed anymore.

### Cost Items
Furthermore, Lexgate requires information about the costs to consider. You can record Invoices in {{<lga-nav text="Cost Items">}} like this:
* {{<lga-lbl text="Title">}}: A user defined title for the costs.
* {{<lga-lbl text="Date">}}: The date for an Invoice (not used in Lexgate).
* {{<lga-lbl text="Amount">}}: The costs amount. If it's a credit, enter the amount with a leading minus ({{<lga-inp text="-25.50">}}).
* {{<lga-lbl text="Billing Period">}}: The Billing Period, in which the amount should be distributed.

### Contracts
It's possible to store Contracts for Cost Centres which receive an Utility Bill. With this functionality you don't need to enter the information when generating new Bills.

* {{<lga-lbl text="Start">}}: The first day of a contract period.
* {{<lga-lbl text="End">}}: The day when the contract ends. Usually the previous day of the succeeding contracts start. You can leave this field empty when the contract does not have a defined end date yet.
* {{<lga-lbl text="Cost Center">}}: The Cost Center, which is the base for the contract. For example the owned flat or the rented parking lot.
* {{<lga-lbl text="Contact">}}: The Contact which represents the contracting party. For example the owner or tenant of a flat.
* {{<lga-lbl text="Set group authorization">}}: Create permission for the contact on the corresponding Group automatically. Users assigned to the Contact can access the Analysis with this permission.

### Create Utility Bills
You have finished all preparations to generate an Utility Bill. Switch to {{<lga-nav text="Consumption Accounting">}} and parameterize for the resulting Documents:

* {{<lga-lbl text="Type">}}: The Type of the Document to be generated:
    * {{<lga-inp text="Consumption Receipt">}}: A detailed overview of all consumptions, but without costs assigned.
    * {{<lga-inp text="Consumption Bill">}}: A bill with the costs according to the Cost Centre structure.
* {{<lga-lbl text="Billing Period">}}: The desired Billing Period
* {{<lga-lbl text="Template">}}: The Template of the Document to be generated.
* {{<lga-lbl text="Folder">}}: The Folder, in which the Documents to be generated should be stored.
* {{<lga-lbl text="Sender">}}: If selected, this Sender will be set to all Documents to be generated.
* {{<lga-lbl text="Creditor">}}: If selected, this Creditor will be set to all Documents to be generated.
* {{<lga-lbl text="Consumption periods from contracts">}}: If selected, the consumption periods are set automatically depending on the assigned Contracts. If there is no contract for a Cost Center defined, no Document is generated.

Below the Input fields a table is generated which shows all Contracts, the assigned Cost Centres and the calculated Costs. Please check the Calculations.

If all Costs are determined correctly, you can create all Documents by clicking on {{<lga-btn text="Generate">}}. The generation process can take up to 3 Seconds per Document. Further infomration how to process the generated Documents are described [here]({{<relref "/document-management/documents">}}).