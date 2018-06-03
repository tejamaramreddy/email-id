import textract
import re
import smtplib
resume=textract.process('C:\Users\HP\Desktop/resume.docx')
email = re.findall(r'[\w\.-]+@[\w\.-]+', resume)
print "email id of person:" ,email[0]
server = smtplib.SMTP('smtp.gmail.com', 587)
server.starttls()
server.login("userforusing321@gmail.com", "userforusing321@")
 
msg = "HELLO SIR "
server.sendmail("userforusing321@@gmail.com", email, msg)
server.quit()
