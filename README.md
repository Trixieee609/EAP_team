# EAP_team
A project for Code for Good
import pandas as pd
import numpy as np

print("Hello! It seems our system doesn't recognize you. Will you please enter your name here? ")
name=str(input("Hello. I am ..."))
print("Welcome to the program", name,"! This is the Employee Assistance Program (EAP) designed to provide counseling services that range from overwhelming matters to stress and grief. It’s helpful to think of an EAP as a starting point that directs employees to more long-term help. ")
print("Due to the increase in shortage of healthcare staff because of the lack of stability in terms of work environments, we want to guide you on this journey for a stronger version of yourself. \nBeing in this field is tough. You’re not alone in this :]")
print("Our job is to maintain Employee Retention. This would basically mean that we want to ensure you have a good time here and stay with your company for the long term, and reap what you sowed of course!") 
print("Meanwhile our main mission- ‘To serve as a guiding light’ especially for those who need it the most. ")
print("So,", name, "Since it’s your first time here, we’ll start off with some questions to get to know you. Remember to answer honestly so we can give the most accurate feedback!" )

print("\n")
bad=[]
good=[]
print("1 - Dissatisfied \n2 - Somewhat dissatisfied \n3 - Neutral \n4 - Somewhat satisfied \n5 - Satisfied")

q1=eval(input("Overall, how satisfied are you with your life?"))
if q1>3:
    good.append(1)
elif q1<3:
    bad.append(0)
else:
    pass

q2=eval(input("How happy did you feel yesterday?"))
if q2>3:
    good.append(1)
elif q2<3:
    bad.append(0)
else:
    pass

q3=str(input("Do you think your health or safety is at risk because of your work? yes/no/don't know"))
if q3=='no':
    good.append(1)
elif q3=='yes':
    bad.append(0)
else:
    pass

q4=str(input("In the last 12 months, have you experienced musculoskeletal problems as a result of work activities? yes/no/don't know"))
if q4=='no':
    good.append(1)
elif q4=='yes':
    bad.append(0)
else:
    pass

q5=str(input("Does your organization take positive action on health and well being? yes/no/don't know"))
if q5=='yes':
    good.append(1)
elif q5=='no':
    bad.append(0)
else:
    pass

print("\n1 - Strongly agree \n2 - Agree \n3 - Neither agree nor disagree \n4 - Disagree \n5 - Strongly disagree")
q6=eval(input("I would be confident talking to my line manager about a mental health problem (which might include anxiety, stress or depression)"))
if q6<3:
    good.append(1)
elif q6>3:
    bad.append(0)
else:
    pass

q7=eval(input("I have an acceptable workload."))
if q7<3:
    good.append(1)
elif q7>3:
    bad.append(0)
else:
    pass

q8=eval(input("Your job requires that you hide your feelings."))
if q8>3:
    good.append(1)
elif q8<3:
    bad.append(0)
else:
    pass

print("\n1 - Always \n2 - Most of the time \n3 - Sometimes \n4 - Rarely \n5 - Never")
q9=eval(input("I am able to successfully balance work and personal life."))
if q9>3:
    good.append(1)
elif q9<3:
    bad.append(0)
else:
    pass

q10=eval(input("I feel that the organization respects setting boundaries to manage work and life. "))
if q10<3:
    good.append(1)
elif q10>3:
    bad.append(0)
else:
    pass

dict1={"NAME": "SUMITA ARORA","CDA LICENCE HOLDER":"YES", "EXPERIENCE":"6 YEARS","EXPERTISE":"Cognitive Behavioral Therapy","CONTACT":"+971 50787####"}
ser1=pd.Series(dict1)
dict2={"NAME":" TOMMY LASCELLES","CDA LICENCE HOLDER":"YES", "EXPERIENCE":"7 YEARS","EXPERTISE":" Dialectical Behavior Therapy","CONTACT":"+971 76865####"}
ser2=pd.Series(dict2)
dict3={"NAME":"KATHERINE COLLINS","CDA LICENCE HOLDER":"YES", "EXPERIENCE":"6 YEARS","EXPERTISE":" Exposure  Therapy","CONTACT":" +971 50656####"}
ser3=pd.Series(dict3)
dict4={"NAME":"LAYLA ABASI","CDA LICENCE HOLDER":"YES", "EXPERIENCE":"8 YEARS","EXPERTISE":"Behavioural Activation Therapy","CONTACT":" +971 76587####"}
ser4=pd.Series(dict4)

final=good+bad
if final.count(0)>=7:
    print("Dang. That's rough, buddy. I hope you know you're enough and we know you're trying your best. Maybe seeing someone will help?")
elif final.count(0)>=5 and final.count(0)<7:
    print("Woah. You've been through so much :[ Do you want to try talking it out?")
elif final.count(0)>=3 and final.count(0)<5:
    print("You're so strong for making it this far, hang in there! Would you like someone to help you out?")
elif final.count(0)==final.count(1):
    print("Hm. You don't have much going on huh? Well, you can still consider seeing someone!")
else:
    print("You're doing great! Would you still like to see our options anyways? Maybe for someone you know atleast?")
    
#print(final)

problem='problem'
while problem!=0:
    print("\na - Stress Management Issues \nb - Decrease the Instances of Stress, or Depression \nc - Helping to Increase their Coping Skills \nd - Low Mood \ne - Reductions in Burnout \nf -  Manage your Intense Emotions \ng - Generalized Anxiety Disorder (GAD) \nh - Panic Disorder") 
    problem=str(input("Please select a specialised area and we'll help you get in touch with a counsellor:  "))
    try:
        print("(Please Note! A CDA Licence stands for a Community Development Authority Licence!)")
        if problem=='a':
            print(ser1)
            print("the credentials of the counsellor")
        elif problem=='b':
            print(ser1)
            print("the credentials of the counsellor")
        elif problem=='c':
            print(ser1)
            print("the credentials of the counsellor")
        elif problem=='d':
            print(ser4)
            print("the credentials of the counsellor")
        elif problem=='e':
            print(ser1)
            print("the credentials of the counsellor")
        elif problem=='f':
            print(ser2)
            print("the credentials of the counsellor")
        elif problem=='g':
            print(ser3)
            print("the credentials of the counsellor")
        elif problem=='h':
            print(ser3)
            print("the credentials of the counsellor")
        else:
            print("I'm afraid that isn't an option.")
    except ValueError:
        print("Please try again.")
    prob=str(input("Would you like to see more? yes/no"))
    if prob=='yes':
        continue
    elif prob=='no':
        problem=0
    else:
        problem=0

print("Thank you for filling out the form", name, "! I hope we managed to make your day just a little better. Hang in there and we hope to see you again!")
print("Sincerely, \nThe EAP Team")

