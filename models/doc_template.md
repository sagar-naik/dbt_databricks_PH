{% docs template %}

# docs_template

### Justifications
- In 1 - 2 sentences describe the purpose and use of this model/table
- Example :
    - This table is used to pull all information that exists on a treatment level, from call connection dates to assigned provider ids.   
### Source/Model Relationships

- Use this section to document the source tables and each related model
- Example:
    - Identify base tables for this model.
    - all have one to one relationships with the final table.
    - Participant is many to one with dim_treatment.
- Source tables should be BigQuery table references and models should be dim_tables

### Fields and Transformations
- This section is used to document the fields coming from each source or model relationship noted in the section above. Also, any key transformations or derived fields.
- Each source and model relationship should link to another markdown (.md) file in dbt

## Markdown Creation Process

1. Navigate to https://dillinger.io/ and copy above template into the markdown text box. Dillinger allows you to visualize what the markdown file will look like.
2. Create new file in the text editor you use for dbt. Name the file the exact same as the dim_model except replace dim_ with doc and instead of '.sql' use '.md' . For example: 'dim_treatment.sql' = 'doc_treatment.md'
3. As seen in this template, add curly bracketed '% docs table_name %'  at the very beginning of the markdown file and '% enddocs %' at the end of the markdown file.
4. Save, commit, and push the changes to production

{% enddocs %}