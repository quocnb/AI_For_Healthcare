# AI_For_Healthcare
Udacity Nano Degree Program

### Lesson 2: Clinical Foundations of 2D Medical Imaging

#### 10. Apply Machine Learning Exercise

Create waiting time column

```python
worklist['waiting_time'] = worklist.index * READ_TIME_IN_MINUTES
```

For getting max probability of 2 columns

```python
worklist['max_prob'] = worklist[["Brain_bleed_probability", "Aortic_dissection_probability"]].max(axis=1)
```

Sorting

```python
worklist_prioritized = worklist.sort_values(by=['max_prob'],ascending=False)
```
