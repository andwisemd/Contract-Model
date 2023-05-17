# Employment Contract PDF Parsing API Documentation

##

This API documentation provides details about the endpoints and resources available for parsing an uploaded PDF contract and extracting its data into the employment contract data structure. Please note that human verification is required to ensure the accuracy of the extracted data.

### Base URL

```
https://api.joinandwise.com/pdf-parser
```

### Endpoints

#### Upload and Parse Contract PDF

Upload a contract PDF file and parse its contents into the employment contract data structure. Human verification is required to validate the extracted data.

```
POST /parse
```

**Request Parameters**

| Parameter   | Type        | Description                                     |
| ----------- | ----------- | ----------------------------------------------- |
| contractPdf | file (.pdf) | The contract PDF file to be uploaded and parsed |

**Response**

```
Status: 200 OK

{
  "message": "Contract PDF parsing successful. Human verification required.",
  "verificationCode": "ABC123"
}
```

#### Verify Parsed Data

Verify the parsed data extracted from the contract PDF. Human verification is required to confirm the accuracy of the parsed data.

```
PUT /verify/{verificationCode}
```

**Path Parameter**

| Parameter        | Type   | Description                                   |
| ---------------- | ------ | --------------------------------------------- |
| verificationCode | string | The verification code received during parsing |

**Request Body**

```
{
  "parsedData": {
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
        "clin_research_opp": true

,
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
  },
  "verified": true
}
```

**Response**

```
Status: 200 OK

{
  "message": "Parsed data verified successfully. Employment contract created.",
  "contractId": "

abc123"
}
```

#### Retrieve Verified Employment Contract

Retrieve the verified employment contract with the parsed data.

```
GET /contracts/{contractId}
```

**Path Parameter**

| Parameter  | Type   | Description                            |
| ---------- | ------ | -------------------------------------- |
| contractId | string | ID of the verified employment contract |

**Response**

```
Status: 200 OK

{
  "contractId": "abc123",
  "parsedData": {
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
        "gym_memb": true

,
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
  },
  "verified": true
}
```

This API documentation covers the endpoints for uploading and parsing a contract PDF, as well as verifying and retrieving the parsed employment contract. The `POST /parse` endpoint allows you to upload a contract PDF and receive a verification code. Then, using the verification code, you can verify the parsed data using the `PUT /verify/{verificationCode}` endpoint. Finally, you can retrieve the verified employment contract using the `GET /contracts/{contractId}` endpoint, providing the contract ID.

Please note that human verification is required to ensure the accuracy of the parsed data.
