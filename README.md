# Contract-Model
Physician employment contract data model

This data model provides a comprehensive overview of important contractual details for physician agreements. The information modeled here is meant to provide physicians with a useful resource for understanding and negotiating their contracts. The data model is organized into sections that model information relevant to the term of the contract, indemnity provisions, call coverage, benefits, responsibilities, compensation, time off, recourse, and optional fields

The mandatory fields within the data model are organized by type. For example, the term section requires data about the start date, end date, and whether or  not it is eligible for extension. Similarly, the indemnity provisions require data about tail coverage, severance clause, and non-compete.

Optional fields are also included and provide physicians with a way to add more granular details to the agreement. For example, a physician may choose to add details about the specialty, practice setting, geographic area, location, and concierge requirements to the contract.

This data model is built with a focus on physicians and other similar medical professionals. It is meant to provide them with comprehensive information  about the contract so that they can confidently enter into and benefit from it.

Field Name | Data Type | Description | Example 
--- | --- | --- | ---
contract.name | string | Name of agreement | "Mike Smith Physician Agreement"
contract.date_signed | string | Date agreement was signed | "August 1, 2021"
contract.term.start_date | string | Start date of agreement | "August 1, 2021" 
contract.term.end_date | string | End date of agreement | "August 1, 2022" 
contract.term.extension | boolean | Whether or not agreement can be extended | true   
contract.indemnity_provision.tail_ coverage.requirement | boolean | Whether tail coverage is required |  true 
contract.indemnity_provision.severance_clause.amount | number | Severance clause amount | 1000 
contract.indemnity_provision.severance_clause.duration | string | Severance clause duration | 6 
contract.indemnity_provision.non_compete.radius | number | Radius of non-compete | 50  
contract.indemnity_provision.non_compete.duration | number  | Duration of non-compete | 12 
contract.indemnity_provision.non_compete.similarity | string | Similarity of non-compete |  "Family Practice" 
contract.indemnity_provision.non_compete.type | string | Type of non-compete | "Exclusive" 
contract.call_coverage.requirement | boolean | Whether call coverage is required | false 
contract.benefits.health_insurance.types | array | List of health insurance types | [" HMO","PPO","POS","etc."] 
contract.benefits.health_insurance.matching_contribution | number | Amount of matching contribution | 50 
contract.benefits.401K.types | array | List of 401k types | ["Traditional", "Roth", "Etc."] 
contract.benefits.401K.matching_contribution | number | Amount of matching contribution | 100 
contract.responsibilities | array | List of responsibilities | [list_of_responsibilities] 
contract.compensation . | number | Minimum compensation | 40000 
contract.compensation.maximum | number | Maximum compensation | 80000 
contract.compensation.fixed_versus_variable | string | Fixed or variable compensation | "Fixed" 
contract.compensation.performance_metrics| array | List of performance metrics | [list_of_performance_metrics] 
contract.compensation.type | string | Type of compensation | "Fee-for-Service" 
contract.compensation.incentives | array | List of incentives | [list _of_incentives] 
contract.compensation.bonus_structure.minimum | number | Minimum bonus | 5000 
contract.compensation.bonus_structure.maximum | number | Maximum bonus | 10000 
contract.time_off.paid_or_unpaid | array | Paid or unpaid time off |["paid","unpaid "] 
contract.time_off.details.vacation_days | number | Vacation days available | number 
contract.time_off.details.sick_days | number | Sick  days available | number 
contract.time_off.details.holidays | array | List of holidays | [list_of_holidays] 
contract.recourse | array | List of recourse | [list_of_recourse]
contract.optional_fields.specialty | array | List of specialties | [list_of_specialties]
contract.optional_fields.practice_setting | array | Setting of practice | ["academic","hospital","office_based","community","urgent_care"] 
contract.optional_fields.geographic_area | array | Geographic area | ["urban","suburban","rural"] 
contract.optional_fields.location | string | Location of practice | "Smithtown, TX"
contract.optional_fields.professional_liability_coverage | boolean | Whether professional liability coverage is required | true
contract.optional_fields.concierge | boolean | Whether concierge is available | false
