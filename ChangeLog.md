# Change Log
All notable changes to this project will be documented in this file.

## UNRELEASED



## VERSION 2.3
- FIX : Missing icon  *19/10/2022* - 2.3.1
- FIX : update supplier order line from order line *07/10/2022* - 2.3.0  [Pull Request](https://github.com/ATM-Consulting/dolibarr_module_orderfromsupplierordermulticompany/pull/16)

    when const OFSOM_UPDATE_LINE_SOURCE was enabled, the linked supplier order was not updated
    To reproduce :

    First you create an supplier order in "Entity 2" with Company 1 of Entity 1 as Third-Party
    a product line with quantity is 15
    when you validate it, a new Order was created in "Entity 1" with this same product line
    Then you update the last created order line in "Entity 1"
    for example set quantity to 13
    When you enter in "Entity 2" and go to the supplier order, the quantity is still set to 15
    With this fix
    3) The quantity in the supplier order is now updated when you modify in order line

    in this example the quantity is now set to 13



## VERSION 2.2
- FIX: When the third party of the supplier order is not linked to any
  entity, OFSOM should do nothing but instead the user gets a
  MissingEntityLink error
- NEW: Expedition workflow *05/08/2021* - 2.2.0  
  Sur clôture d'une expédition (coté entité fournisseur), permet de faire la reception (coté entité client)

## VERSION 2.1

- Init changelog
