# Employment Contract API Documentation

This API documentation provides details about the endpoints and resources available for managing employment contracts.

### Base URL

```
https://api.joinandwise.com/employment-contracts
```

### Endpoints

#### Retrieve Employment Contract

Retrieve details of a specific employment contract.

```
GET /{contractId}
```

**Path Parameters**

| Parameter  | Type   | Description                   |
| ---------- | ------ | ----------------------------- |
| contractId | string | ID of the employment contract |

**Response**

```
Status: 200 OK

{
  "contractId": "abc123",
  "basicInformation": {
    "emp_type": "Full-time",
    "partnership_track": true,
    "term_prov": "Fixed Term",
    "contract_dur_renew": "1 year"
  },
  "employmentStatusSetting": {
    "emp_status": "Active",
    "prac_size": "Medium",
    "prac_spec": "Family Medicine",
    "prac_set": "Hospital"
  },
  "compensation": {
    "guar_base_sal": 100000,
    "inc_bonus": 5000,
    "profit_share": 0.1,
    "stock_opts": 100,
    "perf_bonus": 10000,
    "ann_raise": 0.05,
    "ret_bonus": 20000
  },
  "workSchedule": {
    "work_hours_sched_req": 40,
    "call_sched": "On-Call Rotation",
    "flex_sched": true,
    "remote_work": false
  },
  "benefits": {
    "timeOff": {
      "vacation_days": 20,
      "sick_days": 10,
      "holidays": 10,
      "personal_leave": 5,
      "parental_leave": 12,
      "bereavement_leave": 3,
      "sabbatical_leave": 3
    },
    "insuranceCoverage": {
      "health_ins": true,
      "dental_ins": true,
      "vision_ins": true,
      "life_ins": true,
      "disability_ins": true,
      "malpractice_cov": true,
      "prof_liab_ins": true,
      "pet_ins": false
    },
    "retirementFinancialBenefits": {
      "retire_benefits": true,
      "retire_plan": "401(k)",
      "health_sav_acct": true,
      "loan_repay_assist": true,
      "flex_spend_acct": true,
      "tuition_reimb": true,
      "student_loan_assist": true
    },
    "professionalDevelopmentEducation": {
      "cont_edu_allow": 1000,
      "cme_days": 5,
      "prof_devel": "Continuing Medical Education",
      "mentor_prog": true,
      "clin_research_opp": true,
      "fac_appointment": true,
      "paid_prof_devel": true
    },
    "workplaceSupport": {
      "ancillary_staff": true,
      "med_license_exp": true,
      "dea_license_exp": true,
      "board_cert_exp": true,
      "member_dues": true,
      "promo_opp": true,
      "med_director": true,
      "comm_outreach": true
    },
    "wellnessWorkLifeBalance": {
      "wellness_prog": true,
      "emp_assist_prog": true,
      "emp_discounts": true,
      "paid_parent_leave": true,
      "childcare_assist": true,


      "work_from_home": true,
      "telemed_opp": true,
      "pet_friendly_work": true,
      "casual_dress": true,
      "gym_memb": true,
      "lunch_ben": true,
      "parking_ben": true,
      "commute_assist": true
    }
  },
  "legalContractualProvisions": {
    "nonCompeteOtherAgreements": {
      "non_comp_clause": true,
      "non_solicit_agree": true,
      "conf_non_disclosure_agree": true,
      "IP_rights": true
    },
    "terminationSeverance": {
      "term_sev_prov": true,
      "dispute_res_proc": "Arbitration"
    },
    "credentialingHospitalPrivileges": {
      "credential_hosp_priv": true,
      "med_license": true,
      "dea_license": true,
      "board_certification": true,
      "membership_dues": true
    },
    "partnershipOwnershipOpportunities": {
      "partnership_buy_in_out": true,
      "ownership_equity_opp": true
    },
    "compensationStructurePaymentFrequency": {
      "comp_struct_pay_freq": "Monthly",
      "reimb_exp_overhead": true
    },
    "reportingStructureSupervision": {
      "report_struct_superv": true,
      "prof_growth_career_adv_opp": true,
      "leader_opp": true,
      "diversity_inclusivity_initiatives": true,
      "cultural_competence_training": true,
      "team_building_activities": true
    },
    "performanceEvaluationFeedback": {
      "perf_eval_criteria": "Objective and Subjective",
      "perf_eval_freq": "Annual",
      "peer_feedback": true,
      "ongoing_mentorship": true
    },
    "relocationAssistanceSigningBonuses": {
      "reloc_assist": true,
      "sign_bonus": 5000
    },
    "miscellaneousProvisions": {
      "appendix_docs": true,
      "contract_amendments": true,
      "governing_law": "California",
      "jurisdiction": "San Francisco",
      "force_majeure": true,
      "unforeseen_circumstances": true,
      "indemnification": true,
      "liability": true,
      "notice_communication": true,
      "contact_info": true,
      "communication_methods": true,
      "entire_agreement": true,
      "amendment_clause": true,
      "arbitration_clause": true,
      "mediation_clause": true,
      "waiver_breach_clause": true
    }
  }
}
```

#### Update Employment Contract

Update the details of a specific employment contract.

```
PUT /{contractId}
```

**Path Parameters**

| Parameter  | Type   | Description                   |
| ---------- | ------ | ----------------------------- |
| contractId | string | ID of the employment contract |

**Request Body**

```json
{
  "basicInformation": {
    "emp_type": "Full-time",
    "partnership_track": true,
    "term_prov": "Fixed Term",
    "contract_dur_renew": "1 year"
  },
  "employmentStatusSetting": {
    "emp_status": "Active",
    "prac_size": "Medium",
    "prac_spec": "Family Medicine",
    "prac_set": "Hospital"
  },
  "compensation": {
    "guar_base_sal": 100000,
    "inc_bonus": 5000,
    "profit_share

": 0.1,
    "stock_opts": 100,
    "perf_bonus": 10000,
    "ann_raise": 0.05,
    "ret_bonus": 20000
  },
  "workSchedule": {
    "work_hours_sched_req": 40,
    "call_sched": "On-Call Rotation",
    "flex_sched": true,
    "remote_work": false
  },
  "benefits": {
    "timeOff": {
      "vacation_days": 20,
      "sick_days": 10,
      "holidays": 10,
      "personal_leave": 5,
      "parental_leave": 12,
      "bereavement_leave": 3,
      "sabbatical_leave": 3
    },
    "insuranceCoverage": {
      "health_ins": true,
      "dental_ins": true,
      "vision_ins": true,
      "life_ins": true,
      "disability_ins": true,
      "malpractice_cov": true,
      "prof_liab_ins": true,
      "pet_ins": false
    },
    "retirementFinancialBenefits": {
      "retire_benefits": true,
      "retire_plan": "401(k)",
      "health_sav_acct": true,
      "loan_repay_assist": true,
      "flex_spend_acct": true,
      "tuition_reimb": true,
      "student_loan_assist": true
    },
    "professionalDevelopmentEducation": {
      "cont_edu_allow": 1000,
      "cme_days": 5,
      "prof_devel": "Continuing Medical Education",
      "mentor_prog": true,
      "clin_research_opp": true,
      "fac_appointment": true,
      "paid_prof_devel": true
    },
    "workplaceSupport": {
      "ancillary_staff": true,
      "med_license_exp": true,
      "dea_license_exp": true,
      "board_cert_exp": true,
      "member_dues": true,
      "promo_opp": true,
      "med_director": true,
      "comm_outreach": true
    },
    "wellnessWorkLifeBalance": {
      "wellness_prog": true,
      "emp_assist_prog": true,
      "emp_discounts": true,
      "paid_parent_leave": true,
      "childcare_assist": true,
      "work_from_home": true,
      "telemed_opp": true,
      "pet_friendly_work": true,
      "casual_dress": true,
      "gym_memb": true,
      "lunch_ben": true,
      "parking_ben": true,
      "commute_assist": true
    }
  },
  "legalContractualProvisions": {
    "nonCompeteOtherAgreements": {
      "non_comp_clause": true,
      "non_solicit_agree": true,
      "conf_non_disclosure_agree": true,
      "IP_rights": true
    },
    "terminationSeverance": {
      "term_sev_prov": true,
      "dispute_res_proc": "Arbitration"
    },
    "credentialingHospitalPrivileges": {
      "credential_hosp_priv": true,
      "med_license": true,
      "dea_license": true,
      "board_certification": true,
      "membership_dues": true
    },
    "partnershipOwnershipOpportunities": {
      "partnership_buy_in_out": true,
      "ownership_equity_opp": true
    },
    "compensationStructurePaymentFrequency": {
      "comp_struct

_pay_freq": "Monthly",
      "reimb_exp_overhead": true
    },
    "reportingStructureSupervision": {
      "report_struct_superv": true,
      "prof_growth_career_adv_opp": true,
      "leader_opp": true,
      "diversity_inclusivity_initiatives": true,
      "cultural_competence_training": true,
      "team_building_activities": true
    },
    "performanceEvaluationFeedback": {
      "perf_eval_criteria": "Objective and Subjective",
      "perf_eval_freq": "Annual",
      "peer_feedback": true,
      "ongoing_mentorship": true
    },
    "relocationAssistanceSigningBonuses": {
      "reloc_assist": true,
      "sign_bonus": 5000
    },
    "miscellaneousProvisions": {
      "appendix_docs": true,
      "contract_amendments": true,
      "governing_law": "California",
      "jurisdiction": "San Francisco",
      "force_majeure": true,
      "unforeseen_circumstances": true,
      "indemnification": true,
      "liability": true,
      "notice_communication": true,
      "contact_info": true,
      "communication_methods": true,
      "entire_agreement": true,
      "amendment_clause": true,
      "arbitration_clause": true,
      "mediation_clause": true,
      "waiver_breach_clause": true
    }
  }
}
```

**Response**

```
Status: 200 OK

{
  "message": "Employment contract updated successfully."
}
```

This API documentation covers the endpoints for retrieving and updating employment contracts, providing detailed information about the contract's basic information, employment status and setting, compensation, work schedule, benefits, and legal and contractual provisions.
