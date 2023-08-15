# Datasets used
- [Kaggle - Goodreads Books dataset with user rating: 2M](https://www.kaggle.com/datasets/b2dde9353c9d10c36e4d6b593a74c109dbaca6393a1ca0f2c7abafeba7633641)
## Exploration with SQL
---
- Q1. Finding total records
	- Q1.1: Find total number of records in books table
		- ![[q1.png]]
	- Q1.2: Find total number of records in users table
		- ![[q2.png]]
- Q2. Finding missing records
	- Q2.1: Find missing or empty records in Name column of books table
		- ![[Pasted image 20230812142256.png]]
	- Q2.2: Find missing or empty records in Authors column of books table
		- ![[Pasted image 20230812142249.png]]
	- Q2.3: Find missing or empty records in Publisher column of books table
		- ![[Pasted image 20230812142111.png]]
	- Q2.4: Find missing or empty records in ISBN column of books table
- Q3. Exploring duplicate entries
	- Q3.1: finding duplicate entries based on ISBN column
		- ![[Screenshot from 2023-08-12 14-53-00.png]]
		>Here we see that lots of records (exactly 12, original-1, duplicate-11) have ISBN as its dummy value, so we need to explore this records if they are same or different. Similarly randomly check any of its duplicated ISBN records if they are same or different.
	- q3.1.1 check the records which have ISBN field value as 'ISBN'
		- ![[Pasted image 20230812151815.png]]
		> I found that these are redundant dummy entries, so next I need to drop them.
	- q3.1.2 dropping these 12 entries
		- ![[Pasted image 20230812160217.png]]
	- checking records which have empty string as their ISBN value
		- ![[Pasted image 20230812154845.png]]
		> we can see that these are unique books which only have their ISBN field as empty, so no need to drop them
	- q.3.1.3 checking some random records which have same ISBN value
		- ![[Pasted image 20230812153948.png]]
		> we can see that these records are exactly same except the rating distribution 4, which is irrelevant in this case. So next we need to drop these records
	- dropping records having same ISBN value
		- done
	- 
- Q6: Findin duplicate entries where it has Name, Authors and Publisher field same value
	- ![[Pasted image 20230812144336.png]]

## Modular Coding
### create the directory structure
- make a template.py and define the directory structure there
	- j
### make logger and exception handler
- make the logger file in src/recSys/__init__.py
- we can later call the logger by <code>from recSys import logger</code>

	```python
	import os
	import sys
	import logging
	
	logging_str = "[%(asctime)s: %(levelname)s: %(module)s: %(message)s]"
	
	log_dir = "logs"
	log_filepath = os.path.join(log_dir,"running_logs.log")
	os.makedirs(log_dir, exist_ok=True)
	
	
	logging.basicConfig(
	    level= logging.INFO,
	    format= logging_str,
	
	    handlers=[
	        logging.FileHandler(log_filepath),
	        logging.StreamHandler(sys.stdout)
	    ]
	)
	
	logger = logging.getLogger("recSysLogger")
	
	 ```
## update .yaml files
- update config.yaml
- update schema.yaml
- update params.yaml
### updating entities
- update the entities in src/recSys/entity/config_entity.py
### update configuration manager
- update src/config/configuration.py
### update the components
- update src/components/data_ingestion.py
- update src/components/data_validation.py
### update pipeline
- add each components process in serial order in pipeline
	- l
### update main.py

