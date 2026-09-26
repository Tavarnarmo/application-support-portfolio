# Incorrect invoice amount

## Problem

The user reported that WolfERP had calculated an incorrect amount on invoice FV/2026/09/1842. The invoice amount should have been 1230 PLN, but the system calculated 1476 PLN.

## Diagnostics

I opened the invoice and checked its line items. I found an additional line item, “Express service”, which explained the difference in the invoice amount.
I asked the user whether the “Express service” line item should be included on the invoice. The user confirmed that she hadn't selected this option.
I checked the document history and found that the “Express service” line item had been added automatically by RULE-SALES-07. 
Then I checked the documentation for RULE-SALES-07 to find out under which conditions the rule should add the “Express service” line item. 
This didn't help because the documentation contained two contradictory pieces of information.
I escalated the case to L2 support and asked for clarification regarding the contradictory information in the documentation.
L2 explained that the rule had been changed the previous day during deployment and one of the conditions had been configured incorrectly.

## Root cause

The rule had been changed the previous day during deployment, and one of its conditions had been configured incorrectly.

## Resolution

The administrator corrected RULE-SALES-07. I then informed the user about the issue and asked her to reopen the invoice and check whether the amount was correct.
