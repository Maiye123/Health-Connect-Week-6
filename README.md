# Health-Connect-Week-6

Building on the Week 5 exploratory analysis, Week 6 focused on deepening and validating the key findings and translating them into decision support for HealthConnect Clinic.

### Advanced Analysis

The analysis focused on the relationships between:

- Previous no-show history and booking lead time
- Reminder status and previous no-show history
- Appointment type and booking lead time

A key finding was that no-show rates increased across longer booking lead-time bands and higher levels of previous no-show history.

The 31 to 60 day booking lead-time segment recorded elevated no-show rates across all appointment types:

| Appointment Type | No-Show Rate |
|---|---:|
| Follow-up | 65.1% |
| Diagnostic Test | 59.6% |
| Specialist Consultation | 59.2% |
| General Consultation | 58.1% |

This showed that the elevated no-show pattern for longer booking lead times was not concentrated in a single appointment type.

### Cross-Track Integration with Data Science

The Data Analytics findings were shared with the Data Science track for validation and modelling support.

Four key findings were independently recomputed using the Data Science team's prepared dataset:

| Finding | Data Analytics | Data Science |
|---|---:|---:|
| Previous no-shows | 43.5% → 68.8% | 46.3% → 70.3% |
| 31 to 60 day lead time | 60.5% | 63.9% |
| Reminder: Yes vs No | 47.4% vs 51.4% | 49.9% vs 54.6% |
| Distance ≥20 km | ~58% | 60.2% |

The results showed that both tracks were observing the same underlying patterns in the HealthConnect data.

### Modelling Impact

Two analytics-driven feature engineering suggestions were tested by the Data Science track:

1. A categorical booking lead-time band matching the bands used in the Data Analytics analysis.
2. A previous no-shows × booking lead-time interaction feature.

Both features were retained after improving the candidate model's ROC AUC from approximately 0.680 to 0.682.

An important modelling insight was also identified. Previous no-show history showed a strong descriptive relationship with missed appointments, but booking lead time and distance ranked higher in predictive importance when multiple variables were considered together.

This demonstrated the difference between descriptive association and incremental predictive contribution.

### Key Recommendations

Based on the validated findings, HealthConnect could consider:

- Prioritising stronger confirmation and follow-up for appointments booked further in advance.
- Providing targeted support for patients with repeated previous no-shows.
- Reviewing reminder strategies and their effectiveness.
- Using multiple factors together when developing appointment support or prediction strategies rather than relying on a single risk indicator.

### Limitations

The analysis identifies associations rather than causal relationships.

The Data Analytics and Data Science analyses produced slightly different percentages because the teams used their respective prepared datasets, but the direction and overall pattern of the findings were closely replicated.

The difference between descriptive association and predictive importance should also be considered when interpreting the results.

### Week 7 Focus

The next stage will focus on testing and refinement, including validating the candidate model, checking whether the analytical patterns remain stable, and assessing the effectiveness of the proposed decision-support approach.
