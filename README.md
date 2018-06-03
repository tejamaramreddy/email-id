# email-id
import textract
import re
resume=textract.process('C:\Users\HP\Desktop/resume.docx')
email = re.findall(r'[\w\.-]+@[\w\.-]+', resume)
print "email id of person:" ,email[0]
