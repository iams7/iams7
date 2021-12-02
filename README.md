```python
class Readme:

    def __init__(self, username="iams7", year=2021):
    
        self.username = username
        self.name = "Sridhar Ram"
        
        self.education = {
            'programming': ['Software Engineering','Computing Science'],
            'architecture': ['Master of Science','VIT University']
        }
        
        self.employment = {
            'developer': ['company', 'city'],
            'software_engineer_1': ['miniOrange Security Software','Pune'],
            'software_engineer_2': ['Langscape Language Solutions pvt. Ltd','Chennai']
        }

    def doing(self, now=2021):
    
        today = self.year
        
        if (now > 2014 and now < 2019):
        
            learn = self.education['programming']
            
            return """
                I am currently learning and practicing up {code} the  skills and learning {code_tech} technologies in VIT University.
            """ . format(
                        code=learn[0],
                        code_tech=learn[1]
                        )
            
        elif (now >= 2019 and now <2020):
        
            experience = self.employment['software_engineer_1']
            return """
                I was a Software engineer at {large_firms} in {big_cities} for 1 year
            """ . format(
                        large_firms=experience[0],
                        big_cities=experience[1]
                        )

        elif (now==today):
        
            dream = self.employment['software_engineer_2']
            level = self.education['programming']
            
            return """
                I am currently a Freelance Software Engineer
                and a FTE in {current_company} which motivates me 
                to make progress on my {code_tech} skills and upgrades
                all the time.
            """ . format(
                        current_company=dream[0],
                        code_tech=level[0]
                        )

        elif (now>today):
        
            goal = self.employment['developer']
            
            return """
                I am eager to collaborate with {teams} and {projects}.
            """ . format(
                        teams=goal[0],
                        projects=goal[1]
                        )
        else:
        
            return """
                Hi there!
            """
            
    def collaborate(self, role, organization, location):
    
        opportunity = self.employment
        opportunity[role] = [organization, location]

me = Readme(2021)
```
