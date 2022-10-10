# Kamila Olech

### Scientist

Phone: +48 509 740073
E-mail: kamila.olech@outlook.com
[LinkedIn](https://pl.linkedin.com/in/kamila-olech-5279215a) 
[GitHub](https://github.com/kamilaolech?tab=repositories)

>I am a PhD in Chemistry with seven years of industrial experience in medical chemistry. My current job aim to discover a new anticancer therapy. I am fascinated by the possibility of significantly accelerating this high risk, time and resource consuming process through the implementation of artificial intelligence and machine learning technologies.
Last year I completed postgraduate studies (Mobile and Web Application Tester) and had the opportunity to use the acquired skills while working in the Data Science department at Ryvu Therapeutics (temporary transfer for pregnancy period).
I am looking for an opportunity to start a career in IT. I believe that my creativity, enthusiasm for learning and independence in performing tasks that are key in my current job as a senior scientist will also allow me to be successful in IT. 

#### Education:
* Mobile and Web Application Tester at WSB University (postgraduate studies)   
October 2020 – June 2021 


* Doctor of Chemistry at Wrocław University of Technology   
October 2010 – July 2015


* Master of Science in Organic and Organometallic Chemistry at Wrocław University of Technology   
October 2005 – July 2010

#### Experience:
* Senior Scientist – Medicinal Chemist at Selvita S.A./Ryvu Therapeutics S.A., Kraków   
October 2015 – present


* Researcher Fellow at Ruhr University Bochum, Germany   
June 2013 – November 2013


* Lecturer at Science Festival of Lower Silesia   
2013 – 2014


*  Trainee at INNO-Concept GmbH, Strausberg, Germany   
January 2011 – April 2011

#### Technologies:
* Languages: Python, SQL, HTML, CSS   
* Systems: Windows, Linux (Bash)   
* Project management tools: Redmine, Jira   
* Version control systems: Git   
* Repositories:  GitHub, DockerHub   
* CI/CD tools: Travis CI, Jenkins, GitLab   
* PaaS products: Docker, Heroku    
* Website Monitoring solution: StatusCake   
* Web applications testing tools: Selenium, StatusCake   

#### Code example:

Automated login page test (negative) of the XKom app using Python and Selenium Web Driver follow the Page Object Model (POM) and Data Driven Test (DDT), see more on [GitHub](https://github.com/kamilaolech/XKom_app_test/tree/master/Tests):

```python
import unittest
from ddt import ddt, data, unpack

from Pages.ProfilePage import ProfilePage
from Locators.Locators import Locators
from Tests.BaseTest import BaseTest
from TestUtils.XLUtils import get_data

file_path = "Data/data_login_negative.csv"

# Test - przypadek negatywny logowania do konta XKom

@ddt
class TestLogin_negative(BaseTest):

    @data(*get_data(file_path))
    @unpack
    def testLogin(self, email, password, expectedResult):

        driver = self.driver

        # sprawdzenie czy aplikacja jest zainstalowana
        driver.is_app_installed('pl.xkom_2021-04-07.apk')
        # logowanie ze strony home
        profile = ProfilePage(driver)
        profile.click_profile()
        profile.enter_email(email)
        profile.enter_password(password)
        profile.click_login()
        # sprawdzenie bledu
        notices = self.driver.find_elements_by_class_name(Locators.errorNotices_class_name)
        all_notices = []
        for el in notices:
            all_notices.append(el.get_attribute('text'))
        self.assertIn(expectedResult, all_notices)
        print(all_notices)

if __name__ == 'main':
    suite = unittest.TestLoader().loadTestsFromTestCase(TestLogin_negative)
    unittest.TextTestRunner(verbosity=2).run(suite)
```

#### Languages:
Polish: native

Russian – A2

English – B2/C1   

Since 2010, I have been working in an international and multicultural environment where English is the official working language. In my daily work, I obtain information from international scientific databases and journals as well as write and present reports in English. I also prepared manuscripts for peer-reviewed chemical journals and gave lectures in English. I participated in several international conferences and two internships in Germany (nine months) during my doctoral studies. I try to constantly improve my language skills.

#### Courses:
Soft and Management Skills Trainings

Project team building based on the client's needs (24.01.2018) Kraków    
Professional scientific presentations (7-8.06.2017) Kraków    
Effective manager - training preparing for leadership role (26-27.01.2017) Kraków   
A project team building and management (1-2.06.2016) Kraków   
Assertiveness and communication for managers (23- 24.05.2016) Kraków    
Training of autopresentation skills (4.09.2014) Wrocław   
Setting up and managing of spin off/spin out companies (26.05.2014) Wrocław   
Management of research projects (22.05.2014) Wrocław   
Conflict resolution (05.2014) online course   
Time management (05.2014) online course   
Interpersonal communication (05.2014) online course   

Technical Skills Trainings

Microsoft Excel - advanced course (13-15.03.2017) Comarch, Kraków   
Programming in Python language for beginners - workshop (11.2014-02.2015) WCSS, Wrocław   
Computational approaches for bio-marker design: a tree-levels learning workshop (23-27.06.2014) WCSS, Wrocław   
