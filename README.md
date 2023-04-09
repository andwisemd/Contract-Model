# Physician Employment Contract Data Model
Physician employment contracts can be complex and difficult to navigate. This project aims to simplify the process by providing a standardized data model and a user-friendly web application that allows physicians to easily compare various contracts and negotiate better terms. With the help of AI-powered contract analysis, physicians can focus on their career goals and personal preferences while making informed decisions. This repository contains the physician employment contract data model, designed to support side-by-side comparisons and contract negotiation assistance for physicians.

This will be used to power Andwise's physician employment contract analyzer - https://blog.joinandwise.com/?p=contract-analyzer

## Data Model Structure
The data model consists of the following elements:
* Employment contract attributes (e.g., salary, benefits, work hours)
* Contract provisions (e.g., non-compete clause, termination provisions)

The data model is designed to be easily extensible and adaptable to accommodate changes in contract formats and industry standards.

## Next Steps
1. An AI-powered contract analysis tool that extracts key data points from contracts
2. A web application that enables physicians to upload, view, and compare contracts
3. Advanced search and filtering capabilities within the web application
4. A contract negotiation support feature providing personalized recommendations

## Contributing
We welcome contributions from the community to improve the Physician Employment Contract Data Model and its associated tools. If you'd like to contribute, please follow these steps:
1. Fork the repository on GitHub and create a local clone on your machine.2. Create a new branch with a descriptive name to keep track of your changes.
2. Make your changes to the data model or related tools, ensuring proper markdown formatting and adherence to the guidelines provided.
3. Commit your changes with a descriptive commit message, detailing the changes you made and the reasons behind them.
4. Push your changes to your forked repository on GitHub.
5. Open a pull request, explaining your changes and why they should be merged into the main repository.
6. Collaborate with the maintainers to address any revisions or feedback.

Once approved, your changes will be merged into the main repository.

## Fields included:
```emp_type, partnership_track, non_comp_clause, malpractice_cov, moonlighting_pol, call_sched, vac_time, sick_leave, retire_benefits, health_ins, dental_ins, life_ins, disability_ins, reloc_assist, signing_bonus, loan_repay_assist, prof_liab_ins, ancillary_staff, cont_edu_allow, research_fund, mentor_prog, promo_crit, term_prov, perf_review, prof_devel, add_lic_req, patients_per_day, pat_demo, prac_size, prac_spec, prac_set, emp_status, guar_base_sal, inc_bonus, profit_share, stock_opts, cme_days, parental_leave, bereave_leave, flex_sched, remote_work, prod_bonus, pat_satis_bonus, leader_opp, non-comp_clause, malpractice_cov, retire_plan, health_sav_acct, vac_days, sick_days, holidays, reloc_assist, sign_bonus, health_ins, dental_ins, vision_ins, life_ins, disab_ins, prof_liab_ins, student_loan_assist, mentor_prog, clin_research_opp, med_license_exp, dea_license_exp, board_cert_exp, member_dues, promo_opp, fac_appointment, med_director, comm_outreach, emp_assist_prog, wellness_prog, emp_discounts, paid_parent_leave, childcare_assist, tuition_reimb, paid_prof_devel, flex_spend_acct, work_from_home, telemed_opp, sabb_leave, pet_ins, legal_assist, med_mal_ins, reloc_assist, retire_plan, perf_bonus, ann_raise, stock_opts, ret_bonus, vac_days, sick_leave, pers_leave, cme_allow, prof_liab_ins, disab_ins, life_ins, dental_ins, vision_ins, health_ins, mental_health_ben, emp_ref_prog, commute_assist, parking_ben, lunch_ben, gym_memb, wellness_prog, emp_assist_prog, soc_events, vol_opp, parental_leave, childcare_assist, tuition_reimb, flex_sched, laptop_phone, pet_friendly_work, casual_dress, prof_dev, mentor_prog, diversity_inclusion_init, contract_dur_renew, perf_metrics_eval, on_call_comp, OT_pay_pol, work_hours_sched_req, conf_non_disclosure_agree, IP_rights, term_sev_prov, dispute_res_proc, credential_hosp_priv, partnership_buy_in_out, comp_struct_pay_freq, reimb_exp_overhead, report_struct_superv, prof_growth_career_adv_opp, non_solicit_agree, ownership_equity_opp```

Employment Details
------------------

### Basic Information
-   emp_type
-   partnership_track
-   term_prov
-   contract_dur_renew

### Employment Status and Setting
-   emp_status
-   prac_size
-   prac_spec
-   prac_set

### Compensation
-   guar_base_sal
-   inc_bonus
-   profit_share
-   stock_opts
-   perf_bonus
-   ann_raise
-   ret_bonus

### Work Schedule
-   work_hours_sched_req
-   call_sched
-   flex_sched
-   remote_work

Benefits
--------

### Time Off
-   vac_days
-   sick_days
-   holidays
-   pers_leave
-   parental_leave
-   bereave_leave
-   sabb_leave

### Insurance Coverage
-   health_ins
-   dental_ins
-   vision_ins
-   life_ins
-   disability_ins
-   malpractice_cov
-   prof_liab_ins
-   pet_ins

### Retirement and Financial Benefits
-   retire_benefits
-   retire_plan
-   health_sav_acct
-   loan_repay_assist
-   flex_spend_acct
-   tuition_reimb
-   student_loan_assist

### Professional Development and Education
-   cont_edu_allow
-   cme_days
-   prof_devel
-   mentor_prog
-   clin_research_opp
-   fac_appointment
-   paid_prof_devel

### Workplace Support-
-   ancillary_staff
-   med_license_exp
-   dea_license_exp
-   board_cert_exp
-   member_dues
-   promo_opp
-   med_director
-   comm_outreach

### Wellness and Work-Life Balanc
-   wellness_prog
-   emp_assist_prog
-   emp_discounts
-   paid_parent_leave
-   childcare_assist
-   work_from_home
-   telemed_opp
-   pet_friendly_work
-   casual_dress
-   gym_memb
-   lunch_ben
-   parking_ben
-   commute_assist

##Legal and Contractual Provisions
### Non-Compete and Other Agreements
-   non_comp_clause
-   non_solicit_agree
-   conf_non_disclosure_agree
-   IP_rights

### Termination and Severance
-   term_sev_prov
-   dispute_res_proc

### Credentialing and Hospital Privileges
-   credential_hosp_priv

### Partnership and Ownership Opportunities
-   partnership_buy_in_out
-   ownership_equity_opp

### Compensation Structure and Payment Frequency
-   comp_struct_pay_freq
-   reimb_exp_overhead

### Reporting Structure and Supervision
-   report_struct_superv
-   prof_growth_career_adv_opp
-   leader_opp
-   diversity_inclusivity_initiatives
-   cult_compet_train
-   team_building_activities

### Performance Evaluation and Feedback
-   perf_eval_criteria
-   perf_eval_freq
-   peer_feedback
-   ongoing_mentorship

### Relocation Assistance and Signing Bonuses
-   reloc_assist
-   sign_bonus

##Miscellaneous Provisions
### Appendix and Supporting Documents
-   appendix_docs
-   contract_amendments

### Governing Law and Jurisdiction
-   governing_law
-   jurisdiction

### Force Majeure and Unforeseen Circumstances
-   force_majeure
-   unforeseen_circumstances

### Indemnification and Liability
-   indemnification
-   liability

### Notice and Communication
-   notice_communication
-   contact_info
-   communication_methods

### Entire Agreement and Amendment
-   entire_agreement
-   amendment_clause

### Arbitration and Mediation
-   arbitration_clause
-   mediation_clause

### Waiver of Breach
-   waiver_breach_clause

Thank you for your interest in contributing to the Physician Employment Contract Data Model! Together, we can help physicians navigate the complex world of employment contracts and make better-informed decisions for their careers.
