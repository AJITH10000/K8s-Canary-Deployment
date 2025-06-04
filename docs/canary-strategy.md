# Canary Deployment Strategy

## Objective
Deploy two versions of an app using K3s and Istio with traffic splitting:
- 80% to stable (v1)
- 20% to canary (v2)

## Strategy
1. Deploy both versions using Kubernetes manifests.
2. Use Istio VirtualService to split traffic.
3. Monitor logs/metrics via Prometheus/Grafana.
4. Rollback if errors increase; promote canary if stable.
