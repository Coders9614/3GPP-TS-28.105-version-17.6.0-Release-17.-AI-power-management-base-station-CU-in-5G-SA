Use Azure Spot VMs for Non-Critical Inference

Spot VMs let you tap into Azure’s unused compute capacity at deep discounts—up to 70–90% off standard pricing.
🔧 How It Works:
Azure offers spare VM capacity at reduced prices.
You bid for compute, and Azure allocates it only if available.
If Azure needs the capacity back, your Spot VM is evicted with ~30 seconds notice.
Ideal for non-critical AI tasks like batch inference, signal preprocessing, or training retries.

How much does it save?
<img width="754" height="235" alt="Screenshot 2025-09-15 at 11 31 13 AM" src="https://github.com/user-attachments/assets/9413efc9-6a95-450a-bdb1-6ac794213480" />


🧠 Application to Your Project:
Use Spot VMs for pilot signal analysis, offline model training, or data lake ingestion.
Avoid for real-time CU control or latency-sensitive inference.
🔗 Learn more from Databricks’ Spot VM guide.
⚙️ 2. Deploy Azure ML Endpoints with Autoscaling
Azure ML endpoints allow you to deploy models as REST APIs. With autoscaling, you only pay for compute when needed.
🔧 How It Works:
You define scale rules based on metrics like CPU usage, request count, or time of day.
Azure Monitor triggers scale-out or scale-in actions.
You can set min/max instance counts and cooldown periods to avoid flapping.
🧠 Application to Your Project:
Deploy your energy optimization model as an online endpoint.
Autoscale based on:
Number of users connected to CU
Frequency of pilot signal updates
Real-time inference demand
🔗 Full setup guide on Azure ML autoscaling.
📆 3. Consider Reserved Instances for Long-Term Workloads
Reserved Instances (RIs) offer up to 72% savings if you commit to using a VM for 1 or 3 years.
🔧 How It Works:
You reserve a specific VM type in a region.
Azure guarantees availability and locks in a lower price.
You can choose pay upfront or monthly billing.
🧠 Application to Your Project:
Use RIs for:
Continuous CU telemetry processing
Always-on AI inference for energy control
Hosting your RIC xApps/rApps if they run 24/7
