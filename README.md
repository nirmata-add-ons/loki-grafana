# Loki-Grafana

This README documents the Loki-Grafana integration as Nirmata add-on on Kubernetes clusters.

### What is the Loki-Grafana?

Grafana Loki is a set of components that can be composed into a fully featured logging stack.

Loki is built around the idea of only indexing metadata about your logs: labels (just like Prometheus labels). Log data itself is then compressed and stored in chunks in object stores such as S3 or GCS, or even locally on the filesystem. A small index and highly compressed chunks simplifies the operation and significantly lowers the cost of Loki.

### How do I get set up?
1. Clone this repository or add its contents to your own private Git repository.
2. Create a Nirmata catalog application with a Git upstream and select the loki-stack repository. You can optionally select the kustomization.
3. Edit the catalog application and select an add-on category (e.g. Logging). This is required to select the application as an add-on.
4. Update a Cluster Type, or create a new one, and select the loki-stack add-on application in the "Add-Ons" section.Ensure that the namespace you use is "**loki-stack**"
5. Create clusters using the cluster type.
6. If the addon is to be added to a running cluster, create an environment with the name "**loki-stack**" and choose this environment while deploying the application
7. Verify that the application is running in Nirmata. 
8. Access the Grafana dashboard on the exposed node port, the secret "grafana" holds the credentials to access the application.

### Who do I talk to?
For issues, contact support@nirmata.com
