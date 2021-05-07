# C1C-Cost-Optimization

Python script to collect cost-optimization data from Trend Micro Cloud One(TM) Conformity.

## Usage
Create Conformity API Key https://www.cloudconformity.com/help/public-api/api-keys.html  
Install python 3 on your terminal

     $ python C1C_cost_optimisation.py

Set the environment variables to filter the checks API query  
See https://github.com/cloudconformity/documentation-api/blob/master/Checks.md#list-all-account-checks    
Region and accounts list are optional    
CC_REGION is set as us-west-2 by default,    
CC_ACCOUNTIDS is set to include all accounts in the organisation by default  

### Filter options (see checks API documentation)

            "filter[compliances]": os.environ.get("CC_FILTER_COMPLIANCES", ""),
            "filter[createdLessThanDays]": os.environ.get("CC_FILTER_CREATEDLESSTHAN", ""),
            "filter[createdMoreThanDays]": os.environ.get("CC_FILTER_CREATEDMORETHAN", ""),
            "filter[newerThanDays]": os.environ.get("CC_FILTER_NEWERTHANDAYS", ""),
            "filter[olderThanDays]": os.environ.get("CC_FILTER_OLDERTHANDAYS", ""),
            "filter[regions]": os.environ.get("CC_FILTER_REGIONS", ""),
            "filter[resource]": os.environ.get("CC_FILTER_RESOURCE", ""),
            "filter[riskLevels]": os.environ.get("CC_FILTER_RISKLEVELS", ""),
            "filter[ruleIds]": os.environ.get("CC_FILTER_RULEIDS", ""),
            "filter[services]": os.environ.get("CC_FILTER_SERVICES", ""),
            "filter[statuses]": os.environ.get("CC_FILTER_STATUSES", ""),
            "filter[tags]": os.environ.get("CC_FILTER_TAGS", ""),
