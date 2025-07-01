<div id="top">

<!-- HEADER STYLE: CLASSIC -->
<div align="center">

<img src="kubernetes.jpg" width="100%" style="position: relative; top: 0; right: 0;" alt="Project Logo"/>

# HOMELAB

<em></em>

<!-- BADGES -->
<!-- local repository, no metadata badges. -->

<em>Built with the tools and technologies:</em>

<img src="https://img.shields.io/badge/JSON-000000.svg?style=default&logo=JSON&logoColor=white" alt="JSON">
<img src="https://img.shields.io/badge/YAML-CB171E.svg?style=default&logo=YAML&logoColor=white" alt="YAML">

</div>
<br>

---

## Table of Contents

- [Table of Contents](#table-of-contents)
- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
    - [Project Index](#project-index)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
    - [Usage](#usage)
- [Roadmap](#roadmap)
- [Acknowledgments](#acknowledgments)

---

## Overview

<code> 
The purpose of this homelab is to learn more and apply the knowledge about managing kubernetes services locally.
Cluster runs with k3s.
For public access to pods homelab uses cloudflare tunnel with public hostnames and private dns resolution with ingress for Grafana
Currently, secret encryption is handled using SOPS. In the future, this will be migrated to Azure Key Vault.
</code>

---

## Features

<code>❯In progress</code>

---

## Project Structure

```sh
└── homelab/
    ├── apps
    │   ├── base
    │   └── staging
    ├── clusters
    │   └── staging
    ├── infrastructure
    │   └── controllers
    ├── monitoring
    │   └── controllers
    └── renovate.json
```

### Project Index

<details open>
	<summary><b><code>HOMELAB/</code></b></summary>
	<!-- __root__ Submodule -->
	<details>
		<summary><b>__root__</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ __root__</b></code>
			<table style='width: 100%; border-collapse: collapse;'>
			<thead>
				<tr style='background-color: #f8f9fa;'>
					<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
					<th style='text-align: left; padding: 8px;'>Summary</th>
				</tr>
			</thead>
				<tr style='border-bottom: 1px solid #eee;'>
					<td style='padding: 8px;'><b><a href='./homelab/blob/master/renovate.json'>renovate.json</a></b></td>
					<td style='padding: 8px;'>- Renovate.json configures RenovateBot for automated dependency updates<br>- It specifically targets Kubernetes YAML files, ensuring that the projects Kubernetes configurations are kept current with the latest versions of their dependencies<br>- This streamlines the maintenance process and reduces the risk of outdated components within the larger project infrastructure.</td>
				</tr>
			</table>
		</blockquote>
	</details>
	<!-- monitoring Submodule -->
	<details>
		<summary><b>monitoring</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ monitoring</b></code>
			<!-- controllers Submodule -->
			<details>
				<summary><b>controllers</b></summary>
				<blockquote>
					<div class='directory-path' style='padding: 8px 0; color: #666;'>
						<code><b>⦿ monitoring.controllers</b></code>
					<!-- staging Submodule -->
					<details>
						<summary><b>staging</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ monitoring.controllers.staging</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/monitoring/controllers/staging/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>- Kustomization.yaml configures the Kubernetes deployment of the kube-prometheus-stack within the staging environment<br>- It acts as a configuration layer for the monitoring component, integrating pre-defined resources into the broader project infrastructure<br>- This ensures consistent and streamlined deployment of the monitoring stack during the staging phase.</td>
								</tr>
							</table>
							<!-- kube-prometheus-stack Submodule -->
							<details>
								<summary><b>kube-prometheus-stack</b></summary>
								<blockquote>
									<div class='directory-path' style='padding: 8px 0; color: #666;'>
										<code><b>⦿ monitoring.controllers.staging.kube-prometheus-stack</b></code>
									<table style='width: 100%; border-collapse: collapse;'>
									<thead>
										<tr style='background-color: #f8f9fa;'>
											<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
											<th style='text-align: left; padding: 8px;'>Summary</th>
										</tr>
									</thead>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/monitoring/controllers/staging/kube-prometheus-stack/kustomization.yaml'>kustomization.yaml</a></b></td>
											<td style='padding: 8px;'>- Kustomization.yaml configures the deployment of the kube-prometheus-stack in a staging environment<br>- It leverages a base configuration located in <code>monitoring/controllers/base/kube-prometheus-stack/</code> to define the monitoring stacks resources<br>- The absence of a namespace declaration indicates a potential overlay or customization strategy for the base configuration, rather than a standalone deployment<br>- This file facilitates consistent and manageable deployment of the monitoring system across different environments.</td>
										</tr>
									</table>
								</blockquote>
							</details>
						</blockquote>
					</details>
					<!-- base Submodule -->
					<details>
						<summary><b>base</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ monitoring.controllers.base</b></code>
							<!-- kube-prometheus-stack Submodule -->
							<details>
								<summary><b>kube-prometheus-stack</b></summary>
								<blockquote>
									<div class='directory-path' style='padding: 8px 0; color: #666;'>
										<code><b>⦿ monitoring.controllers.base.kube-prometheus-stack</b></code>
									<table style='width: 100%; border-collapse: collapse;'>
									<thead>
										<tr style='background-color: #f8f9fa;'>
											<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
											<th style='text-align: left; padding: 8px;'>Summary</th>
										</tr>
									</thead>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/monitoring/controllers/base/kube-prometheus-stack/kustomization.yaml'>kustomization.yaml</a></b></td>
											<td style='padding: 8px;'>- Kustomization.yaml configures the Kubernetes deployment of the kube-prometheus-stack within the monitoring namespace<br>- It orchestrates the installation of necessary resources, including namespace definition, repository details, release specifications, and Grafana secrets, ensuring a complete and functional Prometheus monitoring system.</td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/monitoring/controllers/base/kube-prometheus-stack/repository.yaml'>repository.yaml</a></b></td>
											<td style='padding: 8px;'>- The <code>repository.yaml</code> file configures a Helm repository for the kube-prometheus-stack within the monitoring component<br>- It specifies the repository URL and update interval, enabling automated updates of the Prometheus monitoring stack deployed via Flux<br>- This ensures the monitoring infrastructure remains current with the latest versions from the Prometheus community.</td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/monitoring/controllers/base/kube-prometheus-stack/namespace.yaml'>namespace.yaml</a></b></td>
											<td style='padding: 8px;'>- The <code>namespace.yaml</code> file defines a Kubernetes namespace named monitoring<br>- It serves as a foundational component within the broader monitoring system, providing dedicated resource allocation and isolation for the kube-prometheus-stack<br>- This ensures the monitoring infrastructure operates independently, enhancing security and organization within the overall project architecture.</td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/monitoring/controllers/base/kube-prometheus-stack/release.yaml'>release.yaml</a></b></td>
											<td style='padding: 8px;'>- The <code>release.yaml</code> file deploys and manages the Kube Prometheus Stack, including Grafana, within the monitoring namespace<br>- It uses FluxCD for automated updates and specifies configuration details such as Grafanas ingress, TLS settings, and persistent storage<br>- The deployment includes creation and management of custom resource definitions (CRDs)<br>- Grafanas persistent storage is defined by a separate PersistentVolumeClaim.</td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/monitoring/controllers/base/kube-prometheus-stack/grafana-secret.yaml'>grafana-secret.yaml</a></b></td>
											<td style='padding: 8px;'>- Grafanas administrative credentials are securely stored<br>- The YAML file defines a Kubernetes secret containing encrypted Grafana admin username and password<br>- Its part of the monitoring system's infrastructure, ensuring secure access to the Grafana dashboard within the kube-prometheus-stack<br>- The encryption protects sensitive data at rest.</td>
										</tr>
									</table>
								</blockquote>
							</details>
						</blockquote>
					</details>
				</blockquote>
			</details>
		</blockquote>
	</details>
	<!-- apps Submodule -->
	<details>
		<summary><b>apps</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ apps</b></code>
			<!-- staging Submodule -->
			<details>
				<summary><b>staging</b></summary>
				<blockquote>
					<div class='directory-path' style='padding: 8px 0; color: #666;'>
						<code><b>⦿ apps.staging</b></code>
					<table style='width: 100%; border-collapse: collapse;'>
					<thead>
						<tr style='background-color: #f8f9fa;'>
							<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
							<th style='text-align: left; padding: 8px;'>Summary</th>
						</tr>
					</thead>
						<tr style='border-bottom: 1px solid #eee;'>
							<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/staging/kustomization.yaml'>kustomization.yaml</a></b></td>
							<td style='padding: 8px;'>- Kustomization.yaml configures Kubernetes deployments<br>- It integrates three applications—Linkding, Cloudflare, and Audiobookshelf—into a staging environment<br>- The file acts as a central point for managing these applications within the broader project structure, simplifying their deployment and configuration<br>- It streamlines the process of deploying and managing multiple microservices.</td>
						</tr>
					</table>
					<!-- audiobookshelf Submodule -->
					<details>
						<summary><b>audiobookshelf</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ apps.staging.audiobookshelf</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/staging/audiobookshelf/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
						</blockquote>
					</details>
					<!-- cloudflare Submodule -->
					<details>
						<summary><b>cloudflare</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ apps.staging.cloudflare</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/staging/cloudflare/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
						</blockquote>
					</details>
					<!-- linkding Submodule -->
					<details>
						<summary><b>linkding</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ apps.staging.linkding</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/staging/linkding/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/staging/linkding/linkding-secret.yaml'>linkding-secret.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
						</blockquote>
					</details>
				</blockquote>
			</details>
			<!-- base Submodule -->
			<details>
				<summary><b>base</b></summary>
				<blockquote>
					<div class='directory-path' style='padding: 8px 0; color: #666;'>
						<code><b>⦿ apps.base</b></code>
					<!-- audiobookshelf Submodule -->
					<details>
						<summary><b>audiobookshelf</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ apps.base.audiobookshelf</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>- Kustomization.yaml` configures the Kubernetes deployment of the audiobookshelf application<br>- It orchestrates the creation of the necessary Kubernetes resources, including namespaces, deployments, services, and persistent storage for audiobooks, podcasts, and metadata<br>- This ensures a complete and properly configured audiobookshelf application within the Kubernetes cluster.</td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/storageConfig.yaml'>storageConfig.yaml</a></b></td>
									<td style='padding: 8px;'>- StorageConfig.yaml<code> defines a persistent volume claim named </code>audiobookshelf-config<code> within the </code>audiobookshelf<code> application<br>- It allocates 1 GiB of storage accessible in read-write mode<br>- This configuration ensures the application has dedicated persistent storage for its configuration data, contributing to the overall data management strategy of the </code>apps/base` component.</td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/service.yaml'>service.yaml</a></b></td>
									<td style='padding: 8px;'>- Audiobookshelf`, internally within the cluster on port 3005<br>- This allows other services within the cluster to communicate with the audiobook shelf application via its internal IP address and port<br>- The service uses a ClusterIP type, limiting access to the clusters internal network.</td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/storageMetaData.yaml'>storageMetaData.yaml</a></b></td>
									<td style='padding: 8px;'>- StorageMetaData.yaml<code> defines a PersistentVolumeClaim named </code>audiobookshelf-metadata<code> within the </code>apps/base/audiobookshelf` application<br>- It allocates 1 GiB of persistent storage with read-write access, ensuring the audiobook shelf application has dedicated, persistent storage for metadata<br>- This contributes to the overall data management strategy of the project.</td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/storagePodcasts.yaml'>storagePodcasts.yaml</a></b></td>
									<td style='padding: 8px;'>- StoragePodcasts.yaml<code> defines a PersistentVolumeClaim named </code>audiobookshelf-podcasts<code> within the </code>audiobookshelf` application<br>- It allocates 1 GiB of persistent storage accessible in read-write mode<br>- This ensures the audiobook application has dedicated, persistent storage for podcast data, contributing to the overall data management strategy of the base application.</td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/audiobookshelf-env.yaml'>audiobookshelf-env.yaml</a></b></td>
									<td style='padding: 8px;'>- The <code>audiobookshelf-env.yaml</code> file configures the Audiobookshelf applications environment variables<br>- It defines a ConfigMap within the Kubernetes cluster, specifying port 3005 for the application<br>- This ensures consistent environment settings across deployments, contributing to the overall applications portability and maintainability within the larger project structure<br>- The ConfigMap simplifies environment management for the Audiobookshelf service.</td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/namespace.yaml'>namespace.yaml</a></b></td>
									<td style='padding: 8px;'>- The <code>namespace.yaml</code> file defines the Kubernetes namespace <code>audiobookshelf</code><br>- It serves as a foundational element within the <code>apps/base/audiobookshelf</code> application, providing dedicated resource isolation and organization for the audiobook shelf applications components within the broader projects Kubernetes deployment<br>- This ensures clean separation of concerns and simplifies management of the application's resources.</td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/storageAudiobooks.yaml'>storageAudiobooks.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/audiobookshelf/deployment.yaml'>deployment.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
						</blockquote>
					</details>
					<!-- cloudflare Submodule -->
					<details>
						<summary><b>cloudflare</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ apps.base.cloudflare</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/cloudflare/cloudflare.yaml'>cloudflare.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/cloudflare/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/cloudflare/cloudflare-secret.yaml'>cloudflare-secret.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/cloudflare/namespace.yaml'>namespace.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
						</blockquote>
					</details>
					<!-- linkding Submodule -->
					<details>
						<summary><b>linkding</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ apps.base.linkding</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/linkding-configmap.yaml'>linkding-configmap.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/storage.yaml'>storage.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/service.yaml'>service.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/linkding-database-secret.yaml'>linkding-database-secret.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/namespace.yaml'>namespace.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/linkding-ingress.yaml'>linkding-ingress.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/apps/base/linkding/deployment.yaml'>deployment.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
						</blockquote>
					</details>
				</blockquote>
			</details>
		</blockquote>
	</details>
	<!-- clusters Submodule -->
	<details>
		<summary><b>clusters</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ clusters</b></code>
			<!-- staging Submodule -->
			<details>
				<summary><b>staging</b></summary>
				<blockquote>
					<div class='directory-path' style='padding: 8px 0; color: #666;'>
						<code><b>⦿ clusters.staging</b></code>
					<table style='width: 100%; border-collapse: collapse;'>
					<thead>
						<tr style='background-color: #f8f9fa;'>
							<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
							<th style='text-align: left; padding: 8px;'>Summary</th>
						</tr>
					</thead>
						<tr style='border-bottom: 1px solid #eee;'>
							<td style='padding: 8px;'><b><a href='./homelab/blob/master/clusters/staging/apps.yaml'>apps.yaml</a></b></td>
							<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
						</tr>
						<tr style='border-bottom: 1px solid #eee;'>
							<td style='padding: 8px;'><b><a href='./homelab/blob/master/clusters/staging/infrastructure.yaml'>infrastructure.yaml</a></b></td>
							<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
						</tr>
						<tr style='border-bottom: 1px solid #eee;'>
							<td style='padding: 8px;'><b><a href='./homelab/blob/master/clusters/staging/monitoring.yaml'>monitoring.yaml</a></b></td>
							<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
						</tr>
					</table>
					<!-- flux-system Submodule -->
					<details>
						<summary><b>flux-system</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ clusters.staging.flux-system</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/clusters/staging/flux-system/gotk-sync.yaml'>gotk-sync.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/clusters/staging/flux-system/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/clusters/staging/flux-system/gotk-components.yaml'>gotk-components.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
						</blockquote>
					</details>
				</blockquote>
			</details>
		</blockquote>
	</details>
	<!-- infrastructure Submodule -->
	<details>
		<summary><b>infrastructure</b></summary>
		<blockquote>
			<div class='directory-path' style='padding: 8px 0; color: #666;'>
				<code><b>⦿ infrastructure</b></code>
			<!-- controllers Submodule -->
			<details>
				<summary><b>controllers</b></summary>
				<blockquote>
					<div class='directory-path' style='padding: 8px 0; color: #666;'>
						<code><b>⦿ infrastructure.controllers</b></code>
					<!-- staging Submodule -->
					<details>
						<summary><b>staging</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ infrastructure.controllers.staging</b></code>
							<table style='width: 100%; border-collapse: collapse;'>
							<thead>
								<tr style='background-color: #f8f9fa;'>
									<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
									<th style='text-align: left; padding: 8px;'>Summary</th>
								</tr>
							</thead>
								<tr style='border-bottom: 1px solid #eee;'>
									<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/staging/kustomization.yaml'>kustomization.yaml</a></b></td>
									<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
								</tr>
							</table>
							<!-- renovate Submodule -->
							<details>
								<summary><b>renovate</b></summary>
								<blockquote>
									<div class='directory-path' style='padding: 8px 0; color: #666;'>
										<code><b>⦿ infrastructure.controllers.staging.renovate</b></code>
									<table style='width: 100%; border-collapse: collapse;'>
									<thead>
										<tr style='background-color: #f8f9fa;'>
											<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
											<th style='text-align: left; padding: 8px;'>Summary</th>
										</tr>
									</thead>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/staging/renovate/kustomization.yaml'>kustomization.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
									</table>
								</blockquote>
							</details>
							<!-- database Submodule -->
							<details>
								<summary><b>database</b></summary>
								<blockquote>
									<div class='directory-path' style='padding: 8px 0; color: #666;'>
										<code><b>⦿ infrastructure.controllers.staging.database</b></code>
									<table style='width: 100%; border-collapse: collapse;'>
									<thead>
										<tr style='background-color: #f8f9fa;'>
											<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
											<th style='text-align: left; padding: 8px;'>Summary</th>
										</tr>
									</thead>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/staging/database/kustomization.yaml'>kustomization.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
									</table>
								</blockquote>
							</details>
						</blockquote>
					</details>
					<!-- base Submodule -->
					<details>
						<summary><b>base</b></summary>
						<blockquote>
							<div class='directory-path' style='padding: 8px 0; color: #666;'>
								<code><b>⦿ infrastructure.controllers.base</b></code>
							<!-- renovate Submodule -->
							<details>
								<summary><b>renovate</b></summary>
								<blockquote>
									<div class='directory-path' style='padding: 8px 0; color: #666;'>
										<code><b>⦿ infrastructure.controllers.base.renovate</b></code>
									<table style='width: 100%; border-collapse: collapse;'>
									<thead>
										<tr style='background-color: #f8f9fa;'>
											<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
											<th style='text-align: left; padding: 8px;'>Summary</th>
										</tr>
									</thead>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/base/renovate/configmap.yaml'>configmap.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/base/renovate/cronjob.yaml'>cronjob.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/base/renovate/kustomization.yaml'>kustomization.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/base/renovate/namespace.yaml'>namespace.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
									</table>
								</blockquote>
							</details>
							<!-- database Submodule -->
							<details>
								<summary><b>database</b></summary>
								<blockquote>
									<div class='directory-path' style='padding: 8px 0; color: #666;'>
										<code><b>⦿ infrastructure.controllers.base.database</b></code>
									<table style='width: 100%; border-collapse: collapse;'>
									<thead>
										<tr style='background-color: #f8f9fa;'>
											<th style='width: 30%; text-align: left; padding: 8px;'>File Name</th>
											<th style='text-align: left; padding: 8px;'>Summary</th>
										</tr>
									</thead>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/base/database/kustomization.yaml'>kustomization.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/base/database/cluster-database.yaml'>cluster-database.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
										<tr style='border-bottom: 1px solid #eee;'>
											<td style='padding: 8px;'><b><a href='./homelab/blob/master/infrastructure/controllers/base/database/namespace.yaml'>namespace.yaml</a></b></td>
											<td style='padding: 8px;'>Code>❯ REPLACE-ME</code></td>
										</tr>
									</table>
								</blockquote>
							</details>
						</blockquote>
					</details>
				</blockquote>
			</details>
		</blockquote>
	</details>
</details>

---

## Getting Started

### Prerequisites

This project requires the following:

- flux CD
- k3s for kubernetes
- cloudnativepg controller (https://cloudnative-pg.io/documentation/current/quickstart/)
- for encryption: gnupg, sops. age

### Installation

Build homelab from the source and intsall dependencies:

1. **Clone the repository:**

    ```sh
    ❯ git clone ../homelab
    ```

2. **Navigate to the project directory:**

    ```sh
    ❯ cd homelab
    ```
---

## Roadmap

- [X] **`Task 1`**: <strike>k3s Implementation</strike>
- [X] **`Task 2`**: <strike>postgresql for linkding.</strike>
- [ ] **`Task 3`**: Azure Key Vault integration.

---

<details closed>
<summary>Contributing Guidelines</summary>

1. **Fork the Repository**: Start by forking the project repository to your LOCAL account.
2. **Clone Locally**: Clone the forked repository to your local machine using a git client.
   ```sh
   git clone ./homelab/
   ```
3. **Create a New Branch**: Always work on a new branch, giving it a descriptive name.
   ```sh
   git checkout -b new-feature-x
   ```
4. **Make Your Changes**: Develop and test your changes locally.
5. **Commit Your Changes**: Commit with a clear message describing your updates.
   ```sh
   git commit -m 'Implemented new feature x.'
   ```
6. **Push to LOCAL**: Push the changes to your forked repository.
   ```sh
   git push origin new-feature-x
   ```
7. **Submit a Pull Request**: Create a PR against the original project repository. Clearly describe the changes and their motivations.
8. **Review**: Once your PR is reviewed and approved, it will be merged into the main branch. Congratulations on your contribution!
</details>

<details closed>
<br>
<p align="left">
   <a href="https://LOCAL{//homelab/}graphs/contributors">
      <img src="https://contrib.rocks/image?repo=/homelab">
   </a>
</p>
</details>

---

## Acknowledgments

- Credit `mischavandenburg`

<div align="right">

[![][back-to-top]](#top)

</div>


[back-to-top]: https://img.shields.io/badge/-BACK_TO_TOP-151515?style=flat-square


---
