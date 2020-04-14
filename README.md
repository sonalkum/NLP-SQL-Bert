# NLP-SQL with BERT

This repo implements the paper Content Enhanced BERT-based Text-to-SQL Generation (https://arxiv.org/abs/1910.07179) for converting the Natural Language Queries to SQL Queries.
The model is trained using the WikiSql dataset and evaluated on the same.
 

# Software Requirements

python 3.6

records 0.5.3   

torch 1.1.0   

# Steps to Run

1, Data prepare:
Download all origin data(  ) and put them at `data_and_model` directory.

Then run
`data_and_model/output_entity.py`

2, Train and eval:

`train.py`

# Data
One data look:
```
{
	"table_id": "1-1000181-1",
	"phase": 1,
	"question": "Tell me what the notes are for South Australia ",
	"question_tok": ["Tell", "me", "what", "the", "notes", "are", "for", "South", "Australia"],
	"sql": {
		"sel": 5,
		"conds": [
			[3, 0, "SOUTH AUSTRALIA"]
		],
		"agg": 0
	},
	"query": {
		"sel": 5,
		"conds": [
			[3, 0, "SOUTH AUSTRALIA"]
		],
		"agg": 0
	},
	"wvi_corenlp": [
		[7, 8]
	],
	"bertindex_knowledge": [0, 0, 0, 0, 4, 0, 0, 1, 3],
	"header_knowledge": [2, 0, 0, 2, 0, 1]
}
```

# Trained model



