# What this directory is

Configuration written out of a ConfigHub hub (sam) as plain files, one directory for each Space. It is what the hub held when this was written. Nothing here needs the hub.

To run from these files, point Argo CD or Flux at the directory of the Space you run.

If your repository makes its files from something else, Helm values or Kustomize overlays, those do not know about the changes below. The files here do. To keep working from values or overlays, put the changes you care about back there.

## Changed in the hub

| Space | Resource | Value | Now | Why | Who, when | Protected |
|---|---|---|---|---|---|---|
| api-base | Deployment /api | `spec.replicas` | `4` | Four for the sale | bot, 2026-10-30 | yes |
| api-live | Deployment /api | `spec.replicas` | `4` | Four for the sale (from api-base, by change order api-base/sale, approved by admin@local.confighub.dev: Four is right for the sale) | bot, 2026-10-30 |  |
