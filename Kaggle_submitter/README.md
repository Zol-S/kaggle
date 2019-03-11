Kaggle Submitter
================

Installation:
- Create the following folders:
	- _archives_: CSV and ipynb files are stored here in ZIP files.
	- _credentials_: Credentials to access Kaggle and Google Spreadsheet are stored under this folder.
	- _temporary_: Temporary files (Competition leaderboards etc.) will be stored under this folder.
	- _input_: Optional folder (also the name can be changed), copy incoming either to this folder of to the root of the Kaggle submitter script 
- Create a Kaggle token: login to kaggle.com, then click on _My Profile_, _Edit Profile_ and _Create New API Token_ to download __kaggle.json__ and copy it to
`C:\Users\<Windows-username>\.kaggle\kaggle.json` on Windows
`chmod 600 ~/.kaggle/kaggle.json` on Linux.
- Go to https://developers.google.com/sheets/api/quickstart/python to enable Google Sheets API, then download client configuration (aka credentials.json) and copy it under `credentials` folder.

Usage:
- Before every competition, set
    - _kaggle_selected_competition_ variable to the name of the competition
    - _kaggle_user_name_ variable to reflect your username on Kaggle
    - _kaggle_leaderboard_ascending_ if the leaderboard is sorted ascending
    - _google_spreasheet_id_ ID of the Google Spreadsheet to save the scores to
- Before every submission
    - _submission_csv_ copy the submission under the input folder and name is accordingly: input/&lt;text&gt;\_CV&lt;CV score of 5 digits of punctuation&gt;.csv
    - _submission_notebook_ the name of the notebook, that is used to generate the output