# The Analysis
## 1. What are the most in demand skills for the top 3 most popular data roles?
```python
fig, ax = plt.subplots(len(job_titles),1)

for i, job_title in enumerate(job_titles):
    df_plot = df_skills_perc[df_skills_perc['job_title_short'] == job_title].head(5)
    df_plot.plot(kind='barh', x='job_skills', y='skill_percent', ax=ax[i], title=job_title)
    ax[i].legend().set_visible(False)
    fig.tight_layout()
    ax[i].set_xlim(0,80)
```



