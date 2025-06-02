# ArgoCD Manual Installation

This directory contains resources and instructions for manually installing [ArgoCD](https://argo-cd.readthedocs.io/) using `kubectl` with [Kustomize](https://kubectl.docs.kubernetes.io/guides/introduction/kustomize/).

## Overview
- **Purpose:** Deploy ArgoCD to your Kubernetes cluster with custom label selectors using Kustomize overlays and patches.
- **Structure:**
  - `kustomization.yaml`: Main Kustomize configuration.
  - `patches/`: Contains patch files for deployments and stateful sets.
  - `install.txt`: Example installation commands or notes.

## Installation Steps
1. **Customize as Needed:**
   - Edit `kustomization.yaml` and patch files in `patches/` to fit your environment or requirements.
2. **Apply with kubectl:**
   ```sh
   kubectl apply -k .
   ```
3. **Verify Installation:**
   - Check ArgoCD pods and services:
     ```sh
     kubectl get pods -n argocd
     kubectl get svc -n argocd
     ```

## Notes
- This setup uses Kustomize patches to apply custom label selectors (e.g., for node selection or affinity).
- For more information, see the [ArgoCD documentation](https://argo-cd.readthedocs.io/).

---

*Maintained by Jack Tattersall. Last updated: June 2025.*