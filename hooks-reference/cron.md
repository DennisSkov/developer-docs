+++
title = "Cron"
weight = 10

+++

The following hooks are provided for Cron related events.

## AfterCronJob

Runs after all scheduled cron tasks have completed.

#### Parameters

| Variable | Type | Notes |
| -------- | ---- | ----- |
| No input parameters for this hook point. |

#### Response

No response supported

#### Example Code

```
<?php
add_hook('AfterCronJob', 1, function($vars) {
    // Perform hook code here...
});
```

## DailyCronJob

Runs at the very end of the daily automation cron execution.

#### Parameters

| Variable | Type | Notes |
| -------- | ---- | ----- |
| No input parameters for this hook point. |

#### Response

No response supported

#### Example Code

```
<?php
add_hook('DailyCronJob', 1, function($vars) {
    // Perform hook code here...
});
```

## DailyCronJobPreEmail

Runs after tasks have completed but before email report is sent.

#### Parameters

| Variable | Type | Notes |
| -------- | ---- | ----- |
| No input parameters for this hook point. |

#### Response

Return true to surpress email report.

#### Example Code

```
<?php
add_hook('DailyCronJobPreEmail', 1, function($vars) {
    // Perform hook code here...
});
```

## PopEmailCollectionCronCompleted

Executes when the POP email collection cron completes.

#### Parameters

| Variable | Type | Notes |
| -------- | ---- | ----- |
| connectionErrors | array | An array of errors if an error occurred while attempting to connect to one or more mailboxes |

#### Response

No response supported

#### Example Code

```
<?php
add_hook('PopEmailCollectionCronCompleted', 1, function($vars) {
    // Perform hook code here...
});
```

## PreCronJob

Runs before the daily automation cron execution.

#### Parameters

| Variable | Type | Notes |
| -------- | ---- | ----- |
| No input parameters for this hook point. |

#### Response

No response supported

#### Example Code

```
<?php
add_hook('PreCronJob', 1, function($vars) {
    // Perform hook code here...
});
```

