# Delivery analysis

## 1. Flow

The flow goes from planning to development, review, packaging, testing, an approved build, and finally deployment to production.

There are several waiting times in the flow. A pull request waits 4 days for review, the test environment is occupied for 3 days, and an approved build waits for the monthly release window.

There is also rework. Approximately 40% of the changes result in bugs that send the work back to the issue.

## 2. Value stream map

Planning
   ↓
Development (3 days)
   ↓
Waiting for review (4 days)
   ↓
Review (20 minutes)
   ↓
Packaging (45 minutes)
   ↓
Waiting for test environment (3 days)
   ↓
Testing (2 days)
   ↓
Approved build
   ↓
Waiting for monthly release window
   ↓
Deployment (4 hours)
   ↓
Production

Rework can occur when bugs are found during testing and the change goes back to the issue. After deployment, around 25% of releases require intervention the next day.
## 3. The three longest waits

1. Waiting for review: 4 days.
2. Waiting for the test environment: 3 days.
3. Waiting for the monthly release window: the exact waiting time is not given, but it can be a significant delay because releases only happen during the monthly release window.

The first two waiting times are explicitly given in the case. The third one cannot be calculated exactly from the available information.

## 4. DORA metrics

- **Deployment frequency:** approximately once per month, based on the monthly release window.
- **Lead time for changes:** long, mainly because changes spend a significant amount of time waiting between stages. The exact lead time cannot be calculated because the waiting time for the monthly release window is not given.
- **Change failure rate:** approximately 25%, using next-day interventions as an indicator of failed releases in this case.
- **Time to restore service:** 6 hours, based on the manual rollback time.

The DORA metrics show that the delivery process has significant waiting time and that changes sometimes require follow-up work after release.

## 5. Assessment against quality criteria

The delivery process does not fully meet the quality criteria for a good DevOps flow.

- **Small batches:** The case does not give enough information to know whether changes are small, but more frequent and smaller changes could make reviews easier.
- **Fast feedback:** The process does not provide fast feedback because a pull request waits 4 days for review and the test environment is unavailable for 3 days.
- **Automation:** Packaging and deployment are manual, which increases the amount of manual work.
- **Low rework:** The process has significant rework because approximately 40% of changes result in bugs.
- **Short lead time:** The lead time is long because of several waiting periods, especially before review, testing and release.

## 6. What I would change first, and why

I would first focus on reducing the 4-day waiting time for code review. I would encourage smaller and more frequent changes so that pull requests are easier to review. This could make feedback faster and help detect problems earlier.

I would also investigate the high rework rate. Since approximately 40% of changes result in bugs, improving testing and feedback earlier in the flow could reduce rework and improve the overall delivery process.
