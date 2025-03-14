# Summary
<!-- Provide a quick summary of what this PR accomplishes. Focus on the purpose and scope of the conversion work. -->

## Pre-Release Steps
<!-- Checklist of pre-release steps that must be completed before merging. -->
1. [ ] phData: Manually deploy the DAGs to DEV to test and provide links to successful DEV DAG in the [Successful DEV DAG Runs](#successful-dev-dag-runs) section below
1. [ ] phData: Provide a link to a DataManagement Pull Request moving the Task(s) SQL to [RETIRED](https://github.com/alny-commercial-dw/DataManagement/tree/master/0-ALNYLAM/METADATA/tasks/US/RETIRED)
1. [ ] phData: Resolve all PR comments and feedback
1. [ ] phData: Change the `MWAA_ENVIRONMENT` variable to `PRD` in all DAGs to be released
1. [ ] phData: Ensure all related Task conversion issues are noted in the [Related Issue(s)](#related-issues) section below
1. [ ] phData: Schedule a release call for the DAGs

## Release Call Steps

During the release meeting complete these steps:

1. [ ] Alnylam: Execute the related [Task Disable SQL list](#task-disable-sql-list) below
1. [ ] phData: Enable all DAGs in the release meeting
1. [ ] Alnylam: Approve the related Pull Request
1. [ ] phData: Merge the Pull Request

> [!IMPORTANT]
> If any DAGs in the release fail:
>
> 1. all DAGs in the release must be disabled immediately
> 1. the release meeting must be rescheduled after bugfixes are made

## Task List
<!-- List all the tasks being converted in this PR. Example:
- Task Name 1
- Task Name 2
- Task Name 3
-->

## Successful DEV DAG Runs
<!-- Provide links to successful DAG runs in DEV environment that validate these changes. Example:
- [DAG Run for dag_name_1](link-to-dag-run-1)
- [DAG Run for dag_name_2](link-to-dag-run-2)
-->

## Task Disable SQL List
<!-- List all `Task disable` commands executed as part of this PR. Include full SQL statements if applicable. Example: -->

```sql
ALTER TASK schema.task_name1 SET ENABLED = FALSE;
ALTER TASK schema.task_name2 SET ENABLED = FALSE;
```

## Related Issue(s)
<!-- List of issues this PR closes. Use GitHub's "closes" keyword to automatically close issues when merged. Example:
- closes #123
- closes #456
-->
