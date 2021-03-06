# Inferring-Geographic-Migration-Patterns-of-COVID-19-with-MACHINA

# Research Pitch
The rapid spread of COVID-19 revealed how ill-prepared the world was to stop the outbreak of a highly infectious disease. Understanding how diseases spread and the routes they take is crucial for stopping future pandemics. Metastatic and Clonal History INtegrative Analysis (MACHINA) is a program for inferring migration patterns between anatomical sites of tumors using DNA sequencing data. While other methods can recover migration patterns of tumors in the body, MACHINA was designed to recover migration patterns by minimizing the number of migrations and comigrations (sites connected by a migration). This means the program attempts to extract migration patterns with the assumption that a migration between two sites is more likely to reoccur than a new migration to another site. There is, however, the potential to use this powerful tool to infer migration patterns between geographic sites based on DNA sequencing data of COVID-19. Inferring this migration pattern using MACHINA and correlating it to an observable factor such as flight volume or geographic proximity could give us a better understanding of the avenues infectious diseases take to spread across the globe.

# Mentors
Benjamin Raphael-  Professor of Computer Science, Computer Science, Princeton University

Gryte Satas- Postdoctoral Research Associate, Computer Science, Princeton University

# A Day in the Life of an OURSIP Intern
Due to Covid-19, all research was done remotely. I would usually work from late morning to late afternoon and then continue later that night for a few hours. For the first few weeks, my days were spent reading relevant research. After that, I spent my days compiling data, coding ways to parse it into a compatible format, running the data through MACHINA, and coding visualization tools for the results. Since the runtime of MACHINA on large datasets proved unreasonable, I frequently met with my mentor or corresponded with those in his lab via Slack about how to solve this problem. Additionally, throughout the entire program, I met twice a week through zoom with my mentor’s research group where they discussed their research and reviewed related papers. Overall, the days were very open-ended, and I was given the power to decide what direction I wanted to take the research as well as the power over the quality of my results. I would recommend others apply to this program if that freedom appeals to you.

# Results
**Migration Tree:**
MACHINA returns a recovered graph of migrations. Each box is a geographic location connected by an edge. The edges can be thought of as a possible transmission of Covid-19. Parallel edges represent a comigration. Comigrations suggest a closer geographic proximity and/or a fewer edges of top flights between countries according to my findings. 

![image](https://user-images.githubusercontent.com/61328005/96463315-99811c80-11f4-11eb-8d41-9afc9b5afdec.png)

**Spread to Common Flight Path Correlation:**
For every country pair with an equal number of comigrations, we measured the number of edges between them by running a DFS on our graph. From this we saw that there was a strong negative correlation (Pearson Coefficient = -0.8) between number of edges and number of comigrations. Thus, as the number of edges between geographic locations increased, the number of comigrations decreased.

![image](https://user-images.githubusercontent.com/61328005/96463379-a9006580-11f4-11eb-86c6-db63fd5cf81d.png)


# Reference Links
https://github.com/raphael-group/machina
