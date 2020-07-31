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
            'engineer': ['miniOrange Security Software','Pune'],
            'technician': ['GP Computers and Network','Ranipet']
        }

    def doing(self, now=2020):
        today = self.year

        if (now<today):
            experience = self.employeement['engineer']
            return """
            I was a Software engineer at {large_firms} in {big_cities} for 6 months
            """.format(large_firms=experience[0],big_cities=experience[1])

        elif (now==today):
            dream = self.education['programming']
            return """
            I am currently brushing up {code} skills and learning {code_tech} technologies.
            """.format(code=dream[0],code_tech=dream[1])

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
