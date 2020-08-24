```python
class Readme:
    def __init__(self, username="iams7", year=2020):
        self.username = username
        self.name = "Sridhar Ram"
        self.education = {
            'programming': ['Software Engineering','Computing Science'],
            'architecture': ['Master of Science','VIT University']
        }
        self.employeement = {
            'developer': ['company', 'city'],
            'software_engineer': ['miniOrange Security Software','Pune'],
            'hardware_engineer': ['Super Solutions pvt. Ltd','Vellore']
        }

    def doing(self, now=2020):
        today = self.year
        
        if (now > 2014 and now < 2019):
            learn = self.education['programming']
            return """
            I am currently brushing up {code} skills and learning {code_tech} technologies.
            """.format(code=learn[0],code_tech=learn[1])
            
        if (now<today):
            experience = self.employeement['software_engineer']
            return """
            I was a Software engineer at {large_firms} in {big_cities} for 1 year
            """.format(large_firms=experience[0],big_cities=experience[1])

        elif (now==today):
            dream = self.employeement['hardware_engineer']
            level = self.education['programming']
            return """
            I am currently a provenance of {my_startup} that keep progression on my {code_tech} skills and upgrades.
            """.format(my_startup=dream[0],code_tech=level[0])

        elif (now>today):
            goal = self.employeement['developer']
            return """
            I am eager to collaborate with {teams} and {projects}.
            """.format(teams=goal[0],projects=goal[1])
        else:
            return """
            Hi there!
            """
    def collaborate(self, role, organization, location):
        opportunity = self.employeement
        opportunity[role] = [organization, location]

me = Readme(2020)
```
