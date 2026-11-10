# Peon or Portainer: deployment platform versus container manager

Portainer is a UI for managing Docker and Kubernetes resources: containers, images, volumes, stacks. It is excellent for seeing and controlling what is running.

A deployment platform starts from the application side: connect a Git repository, build on push, route a domain with TLS, run previews, roll back.

## Use Portainer when

- You run off-the-shelf images and mostly need a dashboard.
- You manage several Docker hosts and want one view.

## Use a deployment platform when

- You ship your own code and want push to deploy.
- You need per-app environment variables, preview URLs and team roles.

Some teams run both on the same server without trouble.

The side by side comparison of [Peon vs Portainer](https://peon.sh/compare/peon-vs-portainer) goes feature by feature. I work on [Peon](https://peon.sh/).
