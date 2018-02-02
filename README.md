# Bar Passage Batch Uploader
Custom Drupal 7 module using Batch API to import names from an uploaded CSV into nodes

This module is written for a site that tracks names of people who pass bar exams in various jurisdictions.

Batch import form asks for exam jurisdiction, exam date (month & year), and the source of the data being imported (e.g., New York Law Journal). The final field is a file upload for a CSV file. The CSV should be three columns: first name, middle name, and last name (in that order) with no header row.

The batch import is coded to populate a node type named 'person' that contains the following fields:
1. First Name (field_first_name) (text)
2. Middle Name/Initial (field_middle_name) (text)
3. Last Name (field_last_name) (text)
4. State/Jurisdiction (field_state) (list_text)
5. Exam Date (field_exam_date) (datetime)
6. Source (field_source) (text)

Fields 1-3 are mapped from the CSV columns. Fields 4-6 are mapped from form data and will be the same for all created nodes in each batch import.
