## Upgrade Kuberenetes Stack:  WARNING
When upgrading to this version of Kubernetes, rolling back to the previous version is not supported.

## Backup Configuration

Backups are enabled/disabled via the `Enable Backups` radio buttons.

The `Backup Creation Period` duration indicates at what rate backups should be created, in minutes.

The `Backup Retention Period` duration indicates at what rate historical backups should be deleted, in minutes. Backups outside of the retention period are expired after the next successful backup.

The maximum number of backups stored on disk at any given moment follows the equation `ceiling(retention period / creation period)`. For example, a `5` minute creation period with `120` minute retention period would store at most `ceiling(120 / 5)` backups or `24` backups. A conservative estimate for backup size is `50MB`, so the attached network storage should have at least `1.2GB` free space. Backup sizes will vary depending on usage.

If backups are disabled, the values for `Backup Creation Period` and `Backup Retention Period` are ignored.

## Further Reading

See [the wiki](https://github.com/rancher/rancher/wiki/Kubernetes-Management#deployment-types) for further information regarding usage of this template.