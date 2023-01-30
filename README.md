# Contract-Model
Physician employment contract data model

This data model provides a comprehensive overview of important contractual details for physician agreements. The information modeled here is meant to provide physicians with a useful resource for understanding and negotiating their contracts. The data model is organized into sections that model information relevant to the term of the contract, indemnity provisions, call coverage, benefits, responsibilities, compensation, time off, recourse, and optional fields

The mandatory fields within the data model are organized by type. For example, the term section requires data about the start date, end date, and whether or  not it is eligible for extension. Similarly, the indemnity provisions require data about tail coverage, severance clause, and non-compete.

Optional fields are also included and provide physicians with a way to add more granular details to the agreement. For example, a physician may choose to add details about the specialty, practice setting, geographic area, location, and concierge requirements to the contract.

This data model is built with a focus on physicians and other similar medical professionals. It is meant to provide them with comprehensive information  about the contract so that they can confidently enter into and benefit from it.

This will be used to power Andwise's physician employment contract analyzer - https://blog.joinandwise.com/?p=contract-analyzer

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
contract.time_off.paid_or_unpaid | array | Paid or unpaid time off |["paid","unpaid"] 
contract.time_off.details.vacation_days | number | Vacation days available | 10 
contract.time_off.details.sick_days | number | Sick days available | 10 
contract.time_off.details.holidays | array | List of holidays | [list_of_holidays] 
contract.recourse | array | List of recourse | [list_of_recourse]
contract.optional_fields.specialty | array | List of specialties | [list_of_specialties]
contract.optional_fields.practice_setting | array | Setting of practice | ["academic","hospital","office_based","community","urgent_care"] 
contract.optional_fields.geographic_area | array | Geographic area | ["urban","suburban","rural"] 
contract.optional_fields.location | string | Location of practice | "Smithtown, TX"
contract.optional_fields.professional_liability_coverage | boolean | Whether professional liability coverage is required | true
contract.optional_fields.concierge | boolean | Whether concierge is available | false
contract.optional_fields.productivity_threshold | Number | The amount of revenue the physician must generate in order to receive additional compensation | 50000
contract.optional_fields.non-clinical_duties | Array | Array of non-clinical duties that the physician is expected to perform | ["Filing patient records", "Attending meetings", "Administrative duties"]
contract.optional_fields.overtime | Boolean | Whether the physician is expected to work overtime | true
contract.optional_ fields.travel | Boolean | Whether the physician is expected to travel for work | false
contract.optional_fields.physician_back_up | Boolean | Whether the physician is expected to provide back-up coverage for other physicians | true
contract.optional_fields.referral _incentive | Number | The amount of money the physician earns for each referral | 200
contract.optional_fields.referral_threshold | Number | The minimum number of referrals the physician must make to earn an incentive |  10
contract.optional_fields.hours_of_work | Number | The number of hours the physician is expected to work each week | 40
contract.optional_fields.benefits_details  | String | Details of benefits package | "Health Insurance, 401k, etc.”
contract.optional_fields.training | String | Details of any training offered or required | "Board certification review course”
contract.optional_fields.termination | String | Details of the termination process for both employer and employee | "30 days notice required”
contract.optional_fields.incentive_structure | String | Details of the incentive structure for the physician | "Performance bonus based on productivity”
contract.optional_fields.signing_bonus | Number | The amount of the signing bonus | 5000
contract.optional_fields.production_type | String | The type of production bonus: Work RVU or Total Collection | "Work RVU”
contract.optional_fields.bonus_rate | Number | The amount of the bonus rate for the production bonus | 0.06
contract.optional_fields.bonus_threshold | Number | The minimum amount required for the physician to receive a bonus | 10000
contract.optional_fields.relocation_bonus | Number | The amount of the relocation bonus | 10000
contract.optional_fields.tail_coverage | String | The type of tail coverage: Employee Paid, Shared Cost, or Employer Paid  | "Employer Paid”
contract.optional_fields.CME_time | Number | The number of weeks of CME time | 4
contract.optional_fields.CME_allowance | Number | The CME allowance in dollars | 10000
