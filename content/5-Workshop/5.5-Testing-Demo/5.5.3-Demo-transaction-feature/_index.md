---
title : "Demo transaction feature, record receipts & calculate CO₂"
date : 2024-01-01
weight : 3
chapter : false
pre : " <b> 5.5.3. </b> "
---

## Demo transaction feature, record receipts & calculate CO₂

After completing the seeding of carbon credits and carbon balances for demo, you will complete the transaction feature demo. To complete, you need to use the "POS" button is temporarily set on the header of the web page, this button will open a POS interface to simulate the POS terminal setup. After that, you need to enter the MCC seeded in DynamoDB, enter the transaction amount, POS machine ID and POS description. Finally, click on **EXECUTE TRANSACTION** to complete the transaction.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.3-Demo-transaction-feature/1-pos-execute.png" width="80%" />

After the transaction is completed successfully, the POS will return a message response with the transaction details. Turn off the POS, reload the web page and you will get the receipts and the CO₂ accumulated after the transaction and the carbon credits calculated by the system.

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.3-Demo-transaction-feature/2-pos-response.png" width="80%" />

<img src="/fcaj-intership-report-workshop/images/5-Workshop/5.5-Testing-Demo/5.5.3-Demo-transaction-feature/3-profile-response.png" width="80%" />

At this point, you have completed the transaction feature demo, record receipts and calculate CO₂ and also the final step of the demo web, we will try to develop and complete other important features to make NaturEra Green Banking a sustainable project with the ability to develop into a scable eBanking that can develop into a profitable enterprise application.
