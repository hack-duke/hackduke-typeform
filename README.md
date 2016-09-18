# hackduke-typeform

##Typeform instructions
- All typeforms must utilize hidden fields to provide information to the backend. They can be enabled at the bottom of the Typeform editing screen. 
- All typeforms must be given a hidden field with the following format route_(update/receive)_(participant/judge/speaker/mentor) (e.g. route_receive_participant would be the route for new participant registration)
- receive or update refers to whether you are creating a new person or simply updating one
- for update forms, you must also add an email hidden field
- to ensure that the correct person is updated when an update form is sent out, use mailchimp merge tags to fill in the email hidden field so that people can be identified automatically (append email=xxxx to the url)
- the participant/judge/speaker/mentor refers to the role the person will play in an event
- the following roles are currently supported
	* participant
	* judge
	* speaker
	* mentor
- the questions for the forms must contain keywords, which are the model fields (e.g. what is your first name would be a good question for first_name, see the the Ideate Registration typeform for more examples)
- keywords can only be used in ONE question, if it's used in multiple questions, information may be overwritten in the database
- dropdowns can be made by placing the text documents in this repository into the choices option for dropdown
- information for multiple choice questions are also included in this repository
- the type of typeform element that should be used for each question is included in parenthesis
- for all roles, you can include the following keywords/questions
	* email (this field is mandatory) (email)
	* first name (short text)
	* last name (short text)
	* gender (multiple choice - no multiple selections) 
	* dietary restrictions (short text)
	* ethnicity (multiple choice - no multiple selections) 
	* phone (short text)
- for participants, the following are currently supported: 
  * graduation year (multiple choice - no multiple selections)
  * over eighteen (yes/no)
  * attending (used for confirmation) (yes/no)
  * major (dropdown)
  * school (dropdown)
  * website (website)
  * resume (file upload)
  * github (website)
  * travel (recipts used for reimbursements ) (file upload)
  * portfolio (website)
  * skills (short text)
  * track (multiple choice)
  * custom - must be prefixed with Q: (e.g. Q: Why do you want to attend HackDuke?) (short text)
- for mentors, 
	* skills (short text)
	* track (multiple choice)
- for speakers, 
	* topic (short text)
	* date (date)
- for judges, 
	* skills (short text)
