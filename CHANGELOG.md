### v2.1.9 (2021-01-19)
* * *
##### New resources:
* Usages is added. Applicable only for Product Catalog V2

##### New end points:
* hosted_pages#checkout_one-time_payments has been added in hosted_pages resource

##### New attributes:
* auto_close_invoices has been added to customers, subscriptions resources
* metered, usage_calculation have been added to items resources
* create_pending_invoices, auto_close_invoices have been added to subscriptions resources

##### New parameters:
* auto_close_invoices has been added to the endpoint: customers#create_a_customer, customers#list_customers, customers#update_a_customer
* invoice_allocations[invoice_id] has been added to the endpoint: customers#collect_payment_for_customer
* coupon_ids has been added to the endpoint: estimates#create_invoice_for_items_estimate. Applicable only for Product Catalog V2
* subscription[auto_close_invoices] has been added to the endpoint: exports#export_revenue_recognition_reports, exports#export_deferred_revenue_reports, exports#export_subscriptions
* customer[auto_close_invoices] has been added to the endpoint: exports#export_revenue_recognition_reports, exports#export_deferred_revenue_reports, exports#export_customers
* item[metered], item[usage_calculation] have been added to the endpoint: exports#export_items. Applicable only for Product Catalog V2
* subscription_id has been added to the endpoint: invoices#add_one-time_charge_to_a_pending_invoice, invoices#add_non-recurring_addon_to_a_pending_invoice
* subscription_id has been added to the endpoint: invoices#add_a_charge-item_to_a_pending_invoice. Applicable only for Product Catalog V2
* metered, usage_calculation have been added to the endpoint: items#create_an_item, items#list_item. Applicable only for Product Catalog V2
* create_pending_invoices, auto_close_invoices, first_invoice_pending have been added to the endpoint: subscriptions#create_subscription_for_items, subscriptions#update_subscription_for_items,subscriptions#import_subscription_for_items. Applicable only for Product Catalog V2
* create_pending_invoices, auto_close_invoices have been added to the endpoint: subscriptions#list_subscriptions

### v2.1.8 (2020-12-15)
* * *
##### New end points:
* estimate_for_creating_a_customer_and_subscription, cancel_subscription_for_items_estimate, gift_subscription_estimate_for_items have been added in estimate resource. Applicable only for Product Catalog V2
* regenerate_invoice_estimate has been added in estimate resource
* create_a_gift_subscription_for_items has been added in gift resource. Applicable only for Product Catalog V2
* regenerate_invoice has been added in subscription resource

##### New attributes:
* show_description_in_invoices, show_description_in_quotes have been added to the resource item_prices
* tiers[starting_unit_in_decimal], tiers[ending_unit_in_decimal], tiers[price_in_decimal] have been added to the resource differential_prices
* show_description_in_invoices, show_description_in_quotes have been added to the resource item_prices. Applicable only for Product Catalog V2

##### New parameters:
* payment_intent[additional_info] has been added to the endpoints customers#create_a_customer, invoices#create_an_invoice, payment_sources#create_using_payment_intent, subscriptions#create_a_subscription, subscriptions#update_a_subscription, subscriptions#create_subscription_for_customer, subscriptions#reactivate_a_subscription, subscriptions#resume_a_subscription
* payment_intent[additional_info] has been added to the endpoints gifts#create_a_gift_subscription_for_items, invoices#create_invoice_for_items_and_one-time_charges, subscriptions#create_subscription_for_items, subscriptions#update_subscription_for_items. Applicable only for Product Catalog V2
* contract_term[action_at_term_end], contract_term[cancellation_cutoff_period], subscription[contract_term_billing_cycle_on_renewal] has been added to the endpoint estimates#estimate_for_creating_a_subscription. Applicable only for Product Catalog V2
* cancel_at, contract_term_cancel_option, cancel_reason_code have been added to the endpoint estimates#cancel_subscription_for_items_estimate
* event_based_addons has been added to the endpoint estimates#cancel_subscription_for_items_estimate
* redirect_url has been added to the endpoint hosted_pages#accept_a_quote
* token_id, retain_payment_source, card, bank_account, payment_method added have been added to the endpoint invoices#create_an_invoice
* token_id, retain_payment_source, card, bank_account, payment_method added have been added to the endpoint invoices#create_invoice_for_items_and_one-time_charges. Applicable only for Product Catalog V2
* show_description_in_invoices, show_description_in_quotes have been added to the endpoints item_prices#create_an_item_price, item_prices#update_an_item_price. Applicable only for Product Catalog V2

### v2.1.7 (2020-11-26)
* * *
##### New resources:
item_family, item, item_price, attached_item and differential_price are added. Applicable only for Product Catalog V2

##### New end points:
* coupons#create_a_coupon_for_items and coupons#update_a_coupon_for_items have been added in coupon resource. Applicable only for Product Catalog V2
* estimates#estimate_for_creating_a_subscription, estimates#estimate_for_updating_a_subscription and estimates#create_invoice_for_items_estimate have been added in estimate resource. Applicable only for Product Catalog V2
* estimates#advance_invoice_estimate has been added in estimate resource
* exports#export_item_families, exports#export_items, exports#export_item_prices, exports#export_attached_items and exports#export_differential_price have been added in export api. Applicable only for Product Catalog V2
* checkout_new_for_items and checkout_existing_for_items have been added in hosted_pages api. Applicable only for Product Catalog V2
* invoices#create_invoice_for_items_and_one-time_charges, invoices#create_invoice_for_a_charge-item and invoices#add_a_charge-item_to_a_pending_invoice have been added in invoice resource. Applicable only for Product Catalog V2
* quotes#create_a_quote_for_a_new_subscription_items, quotes#create_a_quote_for_update_subscription_items and quotes#create_a_quote_for_charge_and_charge_items have been added in quote resource. Applicable only for Product Catalog V2
* subscriptions#create_subscription_for_items, subscriptions#update_subscription_for_items, subscriptions#import_subscription_for_items and subscriptions#cancel_subscription_for_items have been added in subscription resource. Applicable only for Product Catalog V2
* subscriptions#edit_advance_invoice_schedule, subscriptions#retrieve_advance_invoice and subscriptions#remove_an_advance_invoice_schedules have been added in subscription resource
* unbilled_charges#create_an_invoice_for_unbilled_charges has been added to unbilled_charge resource

##### New attributes:
* item_constraints and item_constraint_criteria have been added in coupon resource. Applicable only for Product Catalog V2
* success_url and failure_url have been added in payment_intent resource
* subscription_items and item_tiers have been added in quoted_subscription resource. Applicable only for Product Catalog V2
* has_scheduled_advance_invoices has been added in subscription resource
* subscription_items, item_tiers and charged_items have been added in subscription resource. Applicable only for Product Catalog V2

##### New parameters:
* item_id and item_price_id have been added to the end point: subscriptions#list_subscriptions, exports#export_revenue_recognition_reports, exports#export_deferred_revenue_reports, exports#export_subscriptions. Applicable only for Product Catalog V2
* invoice_immediately, schedule_type and fixed_interval_schedule have been added to the end point: subscriptions#charge_future_renewals
*  success_url and failure_url have been added to the end points: payment_intents#create_a_payment_intent, payment_intents#update_a_payment_intent

##### New Enum values:
* PLAN_ITEM_PRICE, ADDON_ITEM_PRICE, CHARGE_ITEM_PRICE are added to Entitytype Enum
* ITEM_FAMILY_CREATED, ITEM_FAMILY_UPDATED, ITEM_FAMILY_DELETED, ITEM_CREATED, ITEM_UPDATED, ITEM_DELETED, ITEM_PRICE_CREATED, ITEM_PRICE_UPDATED, ITEM_PRICE_DELETED, ATTACHED_ITEM_CREATED, ATTACHED_ITEM_UPDATED, ATTACHED_ITEM_DELETED, DIFFERENTIAL_PRICE_CREATED, DIFFERENTIAL_PRICE_UPDATED, DIFFERENTIAL_PRICE_DELETED are added to EventType Enum

### v2.1.6 (2020-11-16)
* * *
* New attributes price_in_decimal, tiers[starting_unit_in_decimal], tiers[ending_unit_in_decimal], tiers[price_in_decimal] have been added to the resource addon
* New input parameters price_in_decimal, tiers[starting_unit_in_decimal], tiers[ending_unit_in_decimal], tiers[price_in_decimal] have been added to addons#create_an_addon, addons#update_an_addon apis.
* New attributes unit_amount_in_decimal, quantity_in_decimal, amount_in_decimal, line_item_tiers[starting_unit_in_decimal], line_item_tiers[ending_unit_in_decimal], line_item_tiers[quantity_used_in_decimal], line_item_tiers[unit_amount_in_decimal] have been added to the resources credit_note, credit_note_estimate, invoice, invoice_estimate
* New input parameters line_items[unit_amount_in_decimal], line_items[quantity_in_decimal] have been added to credit_notes#create_credit_note api.
* New input parameters subscription[plan_unit_price_in_decimal], subscription[plan_quantity_in_decimal], addons[quantity_in_decimal], addons[unit_price_in_decimal], event_based_addons[quantity_in_decimal], event_based_addons[unit_price_in_decimal] have been added to estimates#create_subscription_estimate, estimates#create_subscription_for_a_customer_estimate, estimates#update_subscription_estimate, hosted_pages#checkout_new_subscription, hosted_pages#checkout_existing_subscription, quotes#create_a_quote_for_a_new_subscription,  quotes#edit_create_subscription_quote, quotes#create_a_quote_for_update_subscription, quotes#edit_update_subscription_quote,  apis
* New input parameters subscription[plan_quantity_in_decimal], addons[quantity_in_decimal] have been added to estimates#gift_subscription_estimate, gifts#create_a_gift, hosted_pages#checkout_gift_subscription apis
* New input parameters addons[quantity_in_decimal], addons[unit_price_in_decimal], charges[amount_in_decimal] have been added to estimates#create_invoice_estimate, invoices#create_an_invoice, quotes#create_a_quote_for_one-time_charges, quotes#edit_one-time_quote apis
* New input parameter amount_in_decimal has been added to invoices#create_invoice_for_a_one-time_charge api
* Input parameter amount has been made optional to invoices#create_invoice_for_a_one-time_charge api
* New input parameters addon_quantity_in_decimal, addon_unit_price_in_decimal have been added to invoices#create_invoice_for_a_non-recurring_addon
* New input parameters line_items[unit_amount_in_decimal], line_items[quantity_in_decimal], line_items[amount_in_decimal], line_item_tiers[starting_unit_in_decimal], line_item_tiers[ending_unit_in_decimal], line_item_tiers[quantity_used_in_decimal], line_item_tiers[unit_amount_in_decimal] have been added to invoices#import_invoice api
* Input parameters line_item_tiers[starting_unit], line_item_tiers[ending_unit], line_item_tiers[quantity_used], line_item_tiers[unit_amount] have beed made optional in invoices#import_invoice api
* New input parameters addon_quantity_in_decimal, addon_unit_price_in_decimal have been added to invoices#add_non-recurring_addon_to_a_pending_invoice api
* New input parameter invoice_date has been added to invoices#close_a_pending_invoice api
* New attributes tiers[starting_unit_in_decimal], tiers[ending_unit_in_decimal], tiers[price_in_decimal], attached_addons[quantity_in_decimal], event_based_addons[quantity_in_decimal], free_quantity_in_decimal, price_in_decimal have been added to the resource plan
* New input parameters tiers[starting_unit_in_decimal], tiers[ending_unit_in_decimal], tiers[price_in_decimal], attached_addons[quantity_in_decimal], event_based_addons[quantity_in_decimal], free_quantity_in_decimal, price_in_decimal have been added to plans#create_a_plan, plans#update_a_plan apis
* New attribute amount_in_decimal has been added to the resource promotional_credit
* New input parameter amount_in_decimal has been added to promotional_credits#add_promotional_credits, promotional_credits#deduct_promotional_credits, promotional_credits#set_promotional_credits apis
* Input parameter amount has been made optional in promotional_credits#add_promotional_credits, promotional_credits#deduct_promotional_credits, promotional_credits#set_promotional_credits apis
* New attributes unit_amount_in_decimal, quantity_in_decimal, amount_in_decimal have been added to the resource quote
* New attributes addons[quantity_in_decimal], addons[unit_price_in_decimal], addons[amount_in_decimal], event_based_addons[quantity_in_decimal], event_based_addons[unit_price_in_decimal] have been added to the sub resource quoted_subscription
* New attributes unit_amount_in_decimal, quantity_in_decimal, amount_in_decimal have been added to the sub resource quoted_line_group
* New attributes addons[quantity_in_decimal], addons[unit_price_in_decimal], addons[amount_in_decimal], event_based_addons[quantity_in_decimal], event_based_addons[unit_price_in_decimal], plan_free_quantity_in_decimal, plan_quantity_in_decimal, plan_unit_price_in_decimal, plan_amount_in_decimal have been added to the resource subscription
* New input parameters plan_unit_price_in_decimal, plan_quantity_in_decimal, addons[quantity_in_decimal], addons[unit_price_in_decimal], event_based_addons[quantity_in_decimal], event_based_addons[unit_price_in_decimal] have been added to subscriptions#create_a_subscription, subscriptions#create_subscription_for_customer, subscriptions#update_a_subscription, subscriptions#import_a_subscription, subscriptions#import_subscription_for_customer apis
* New input parameter amount_in_decimal has been added to subscriptions#add_charge_at_term_end apis
* Input parameter amount has been made optional in subscriptions#add_charge_at_term_end apis
* New input parameters addon_quantity_in_decimal, addon_unit_price_in_decimal have been added to subscriptions#charge_addon_at_term_end api
* New attributes tiers[starting_unit_in_decimal], tiers[ending_unit_in_decimal], tiers[quantity_used_in_decimal], tiers[unit_amount_in_decimal], unit_amount_in_decimal, quantity_in_decimal, amount_in_decimal have been added to the resource unbilled_charge
* New endpoint transactions#refund_a_payment has been added to the resource transaction
### v2.1.5 (2020-10-15)
* * *
* New optional attribute quoted_subscriptions has been added to the resource quote
* New optional attributes resource_version and updated_at are added to the resource payment_intent
### v2.1.4 (2020-09-29)
* * *

* New attribute included_in_mrr has been added in addon and coupon resource
* New attribute offline_payment_method has been added in subscription and customer resource
* New input parameter included_in_mrr has been added in create_an_addon, update_an_addon, create_a_coupon and update_a_coupon apis.
* New input parameter offline_payment_method has been added in create_a_customer, list_customers, update_a_customer, create_a_subscription, create_subscription_for_customer and list_subscriptions apis
* New input parameter auto_collection has been added in update_a_subscription
* New input parameter subscription[offline_payment_method] has been added in create_subscription_estimate, create_subscription_for_a_customer_estimate, update_subscription_estimate, export_revenue_recognition_reports, export_deferred_revenue_reports, export_subscriptions, checkout_new_subscription and checkout_existing_subscription apis
* New input parameter subscription[auto_collection] has been added in checkout_existing_subscription and update_subscription_estimate apis
* New input parameter customer[offline_payment_method] has been added in export_revenue_recognition_reports, export_deferred_revenue_reports, export_customers and create_a_subscription

### v2.1.3 (2020-09-09)
* * *

* New input parameter currency_code is added in list_addons, list_coupons, list_plans, export_plans, export_addons, export_coupons apis
* New attributes powered_by has been added in card resource
* New input parameters subscription[free_period], subscription[free_period_unit] have been added in create_subscription_estimate, create_subscription_for_a_customer_estimate, update_subscription_estimate apis
* Input parameter invoice[customer_id] is made optional in create_invoice_estimate api
* Input parameter customer_id is made optional in create_an_invoice
* Attribute created_at in dunning_attempts is made optional in the invoice resource
* New attributes free_period and free_period_unit have been added in the Subscription resource
* New enum type free_period_unit has been added with the values:
	DAY,
	WEEK,
	MONTH,
	YEAR
* New enum type powered_by has been added in card resource with the values: 
	IDEAL,
    SOFORT,
    BANCONTACT,
    GIROPAY,
    NOT_APPLICABLE
* New endpoint import_contract_term has been added to the subscription resource
* Attributes status, amount and date inside the linked_payment are made optional in the transaction resource
* New endpoint delete has been added to the virtual_bank_account resource
* New values GIROPAY and DOTPAY have been added to the payment_method_types enum
* New values PAYMENT_SOURCE_EXPIRING and PAYMENT_SOURCE_EXPIRED have been added to the event_type enums
* New value PAYPAL has been added to the gateway enum

### v2.1.2 (2020-07-15)
* * *

* New attributes show_description_in_invoices, show_description_in_quotes have been added in Addon, Plan resource
* New input parameters show_description_in_invoices, show_description_in_quotes have been added for create_an_addon, update_an_addon, create_a_plan, update_a_plan apis
* New attribute create_reason_code has been added in Credit notes resource
* Attribute reason_code is made optional in the Credit notes resource
* New filter parameter create_reason_code is added in list_credit_notes api
* New input parameter refund_reason_code has been added in Credit notes' Refund, Record a refund apis
* Sub-resources parent_account_access and child_account_access have been added in Customer resource
* New attribute use_default_hierarchy_settings has been added in Customer resource
* New endpoint update_hierarchy_settings has been added in Customer resource
* New input parameters use_default_hierarchy_settings,  parent_account_access, child_account_access have been added in link_a_customer api
* New input parameter invoice_notes, coupon_ids, invoice[subscription_id], charges[taxable], charges[tax_profile_id], charges[avalara_tax_code], charges[taxjar_product_code] has been added to create_invoice_estimate api
* New input param cancel_reason_code has been added to export_revenue_recognition_reports, export_deferred_revenue_reports, export_subscriptions, export_credit_notes apis
* New input param coupon_ids has been added to checkout_new_subscription, checkout_existing_subscription apis
* Input param subscription_coupon has been deprecated in checkout_new_subscription, checkout_existing_subscription apis
* New attribute void_reason_code has been added to the Invoice resource
* Attribute cn_reason_code has been made optional in applied_credits, adjustment_credit_notes, issued_credit_notes, linked_credit_note sub-resources
* New attribute cn_create_reason_code has been added in applied_credits, adjustment_credit_notes, issued_credit_notes, linked_credit_note sub-resources
* New input parameter subscription_id, invoice_note, remove_general_note, coupon_ids, charges[taxable], charges[tax_profile_id], charges[avalara_tax_code], charges[taxjar_product_code] have been added to create_an_invoice api
* Input parameter coupon is deprecated from create_an_invoice api
* New filter parameter void_reason_code has been added to list_invoices api
* New input parameter invoice_note, remove_general_note, notes_to_remove[entity_type], notes_to_remove[entity_id] have been added to close_a_pending_invoice api
* New input parameter void_reason_code has been added to void_an_invoice api
* New input parameter credit_note[create_reason_code] has been added to refund_an_invoice, record_refund_for_an_invoice api
* New endpoints import_an_order and delete_an_imported_order have been added to Order resource
* New filter parameter exclude_deleted_credit_notes has been added to list_orders api
* New attribute payment_method_type has been added to payment_intent resource and active_payment_attempt sub-resource
* New input parameter payment_method_type has been added to create_a_payment_intent, update_a_payment_intent api
* New attributes version, contract_term_start, contract_term_end, contract_term_termination_fee have been added to Quotes resource
* New endpoints edit_create_subscription_quote, edit_update_subscription_quote, edit_one_time_quote, extend_expiry_date have beed added to Quotes resource
* New input parameters contract_term[action_at_term_end], contract_term[cancellation_cutoff_period], subscription[contract_term_billing_cycle_on_renewal] have been added to create_a_quote_for_a_new_subscription, create_a_quote_for_update_subscription apis
* New attribute version has been added to quote_line_group sub-resource
* New attribute cancel_reason_code has been added to Subscriptions resource
* New filter parameter cancel_reason_code has been added to list_subscriptions, cancel_a_subscription apis
* New input parameter contract_term_billing_cycle_on_renewal has been added to import_a_subscription, import_subscription_for_customer apis
* New input parameter event_based_addon has been added to cancel_a_subscription api
* New filter parameter is_voided has been added to list_unbilled_charges api
* New event_types MRR_UPDATED, ORDER_DELETED have been added
* New values SOFORT, BANCONTACT have been added to the payment_method_types enum
* New attributes entity_type_description has been added to the line_items sub-resource

### v2.1.1 (2020-04-03)
* * *

* A subresource contract_term has been added in Subscription resource
* New endpoint refund_a_credit_note has been added in Credit notes resource
* New endpoint list_quote_line_groups has been added in Quotes resource
* New endpoint list_contract_terms_for_a_subscription has been added in Subscriptions resource
* New input parameter contract_term_billing_cycle_on_renewal, contract_term[action_at_term_end], contract_term[cancellation_cutoff_period] has been added in create_a_subscription, create_subscription_for_customer, update_a_subscription and reactivate_a_subscription apis
* New input parameter contract_term_cancel_option has been added in cancel_a_subscription api
* New input parameter contract_term[action_at_term_end], contract_term[cancellation_cutoff_period], subscription[contract_term_billing_cycle_on_renewal] has been added in create_subscription_estimate, create_subscription_for_a_customer_estimate, checkout_new_subscription, checkout_existing_subscription apis
* New input parameter business_customer_without_vat_number has been added in create_a_customer and update_billing_info_for_a_customer apis
* New input parameter addons[service_period] replaces the parameter addons[date_from] and addons[date_to] in create_a_quote_for_one-time_charges api
* New input parameter charges[service_period] replaces the parameter charges[date_from] and charges[date_to] in create_a_quote_for_one-time_charges api
* New input parameter consolidated_view has been added in retrieve_quote_as_pdf api
* New input parameter customer[business_customer_without_vat_number] has been added in create_a_subscription, update_a_subscription apis
* New value CHECKOUT_COM has been added in gateway enum
* New value CONTRACT_TERMINATION has been added to eventBasedAddons onEvent enum
* New values IDEAL, GOOGLE_PAY has been added to payment types enum
* New event types CONTRACT_TERM_CREATED, CONTRACT_TERM_RENEWED, CONTRACT_TERM_TERMINATED, CONTRACT_TERM_COMPLETED, CONTRACT_TERM_CANCELLED have been added

### v2.1.0 (2020-02-06)
* * *

* New attribute total_payable and charge_on_aaceptance has been added in Quote.java
* New input parameter cancel_at has been added in cancel_a_subscription api

### v2.0.9 (2020-01-08)
* * * 

* New attribute taxjar_product_code has been added in Addon and Plan resource.
* New input parameter taxjar_product_code has been added in create_an_addon, update_an_addon, create_a_plan and update_a_plan api
* New input parameter taxjar_exemption_category has been added in create_a_customer, update_a_customer , create_a_subscription and import_a_subscription api
* New input parameter no_expiry has been added in gift_subscription_estimate and create_a_gift api
* New attribute no_expiry has been added in Gift resource
* New endpoint update_gift has been added in Gift resource
* New value BUSINESS_CHECKING has been added in AccountType enum
* New value CCD has been added in EcheckType enum
* New event type GIFT_UPDATED has been added
* New enum taxjar_exemption_category has been added

### v2.0.8 (2019-09-13)
* * *

* New endpoints gift_subscription_estimate and create_invoice_estimate have been added in estimate resource.
* New input parameter reference_id in payment_intent has been added in create_a_gift, create_an_invoice, create_using_payment_intent, create_a_subscription, create_subscription_for_customer, update_a_subscription, reactivate_a_subscription, resume_a_subscription, create_a_customer and collect_payment_for_customer api.
* New endpoint record_refund_for_a_payment has been added in transaction resource.

### v2.0.7 (2019-08-27)
* * * 

* New attribute client_profile_id has been added in customer resource.
* New input parameter client_profile_id has been added in create_a_customer, update_a_customer, create_subscription_estimate, create_a_subscription and import_a_subscription api.
* New input parameter payment_intent has been added in create_a_gift, create_an_invoice, reactivate_a_subscription and resume_a_subscription api.
* New input parameter replace_primary_payment_source has been added in create_an_invoice api.
* New attribute currency_code has been added in payment_intent resource.

### v2.0.6 (2019-08-14)
* * *

* New resource payment_intent has been added.
* New input parameter 'id' in payment_intent sub-param has been added in create_a_customer, collect_payment_for_customer, create_using_payment_intent, create_a_subscription, create_subscription_for_customer and update_a_subscription .
* New event_types PAYMENT_INTENT_CREATED and PAYMENT_INTENT_UPDATED have been added.

### v2.0.5 (2019-08-07)
* * *

* New attributes tax_amount_in_local_currency and local_currency_code have been added in line_item_tax sub-resource of credit_note, credit_note_estimate, invoice, invoice_estimate, order and quote resources.
* New attributes sub_total_in_local_currency, total_in_local_currency and local_currency_code have been added in credit_note and invoice resources.
* New input parameter gw_payment_method_id has been added in create_a_customer, collect_payment_for_customer, create_using_payment_intent, create_a_subscription, create_subscription_for_customer and update_a_subscription api.
* New attributes name, invoice_id and notes have been added in quote resource.
* New input parameters name, notes and expires_at have been added in create_a_quote_for_a_new_subscription, create_a_quote_for_update_subscription and create_a_quote_for_one-time_charges api.
* New input parameters id, auto_collection and po_number have been added in convert_a_quote api.

### v2.0.4 (2019-07-22)
* * *

* The attribute ref_tx_id has been added in card resource.
* The attribute custmer_id has been added in credit_note_estimate and invoice_estimate resource.
* The input parameters payment_intent with gateway_account_id and gw_token have been added in create a customer, collect payment for customer, create subscription and create subscription for customer API.
* New enum dunning_type has been added.
* New value vantiv has been added in the gateway enum.
* New value sepa_credit has been added in payment method enum. 
* The attribute dunning_attempts has been added in invoice resource.
* New enpoint create_using_payment_intent has been added in payment_source resouce.
* The input parameter reference_transaction has been added in update card payment source API.
* New endpoint list quote has been added in qoutes resource.
* The attributes initiator_type and three_d_secure have been added in transaction resource.
* New attribute scheme has been added in virtual_bank_account resource.
* New input parameter scheme has been added in create a virtual bank account using permanent token and create a virtual bank account API.

### v2.0.3 (2019-07-08)
* * *

* The resources hierarchy and token are added.
* Value ‘day’ is added in period_unit and shipping_frequency_period_unit .
* The parameters fractional_correction, comment, date_from and date_to are added in Create credit note API.
* The attribute customer_id is added to line_item sub resource of Credit note, Credit note estimate, Invoice, Invoice estimate and Quote.
* Endpoints Link a customer, Delink a customer, Get hierarchy, CreateUsingToken are added.
* The attributes business_customer_without_vat_number and relationship are added to customer resource.
* The filter parameters parent_id, payment_owner_id, invoice_owner_id are added in List customers, Export revenue recognition reports, Export Deferred Revenue Reports and Export customers APIs.
* The parameter token_id is added in Collect payment API.
* Event types hierarchy_created, hierarchy_deleted, token_created, token_consumed and token_expired are added.
* The parameter service_period_in_days is added in Create subscription estimate, Create subscription for customer estimate, Update subscription estimate, Checkout new, Checkout existing, Create subscription for customer quote, Update subscription quote, Create subscription, Create subscription for customer, Update subscription, Import subscription and Import subscription for customer.
* The filter parameter payment_owner is added in Export revenue recognition reports,Export Deferred Revenue Reports, Export Invoice and List Invoice APIs.
* The attribute payment_owner is added to invoice.
* The attributes date_from and date_to are added to Create an invoice, create a invoice for add-on and create a invoice for charge,Create a quote for one-time charges, Add charge at term end and Add add-on at term end.
* The parameter comment is added to Stop dunning, Apply payments, Apply credits, Add charge, Add add-on charge, Update details and Close Invoice APIs.
* The parameter ‘claim_credits’ is added to delete invoice API.
* The attribute override_relationship is added to subscription resource.
* The parameter token_id is added to Create subscription API.
* The parameter override_relationship is added to Create subscription for customer and Update subscription APIs.
* The attribute service_period_in_days is added to event add ons sub resource.

### v2.0.2 (2019-04-11)
* * *

* The attributes avalara_sale_type, avalara_transaction_type and avalara_service_type are added in Addon and plan resource.
* The input parameters avalara_sale_type, avalara_transaction_type , avalara_service_type are added in create addon , update addon  ,create plan , update  plan, create invoice  , create invoice for charge, add_charge , add_charge_at_term_end and create_for_onetime_charges api endpoints.
* The attributes is_partial_tax_applied, is_non_compliance_tax and taxable_amount are added in line_item_taxes of credit_note ,credit_note_estimate , invoice, invoice_estimate , quote and order resources.
* The attributes exemption_details and customer_type are added in customer resource .
* The input parameters exemption_details and customer_type are added in create customer, update customer , create subscription estimate, create subscription and import subscription api endpoints.
* The enum values federal and unincorporated are added in tax_juris_type.
* The enum value export is added in tax_override_reason .
* The input parameter cancelled_at is added in cancel order api endpoint.
* New endpoint delete_local is added in payment_source and virtual_bank_account resources.

### v2.0.1 (2019-03-07)
* * *

* The attributes created_at, resource_version and updated_at are added in card, payment_source and virtual_bank_account resources.
* The input filter parameter sort_by with updated_at attribute is added in list customer and list subscription api endpoints.
* New endpoint export orders is added in export resource.
* New endpoint accept quote is added in hosted_pages resource.
* The input filter parameters updated_at and created_at are added in list payment_source api endpoint and list virtual_bank_accounts endpoint .
* New endpoint delete an offline transaction is added in transaction resource.

### v2.0.0 (2019-01-10)
* * *

Chargebee [API V2](https://apidocs.chargebee.com/docs/api#versions) for golang is now live!
