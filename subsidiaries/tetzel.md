---
layout: default
title: Tetzel Institute
description: Satirical subsidiary deploying the Doctrine of Strict Liability against AI hallucination.
permalink: /subsidiaries/tetzel/
---

<p class="eyebrow">OPERATING SUBSIDIARY</p>
<h1>Tetzel Institute</h1>
<p class="dek"><em>Moral Accountability as a Service. Accuracy is expensive. Absolution is cheap.</em></p>

## Mission

Productize moral accountability for stochastic systems via a lightweight indulgence-payment protocol. Tetzel sits in front of AI agents and accepts confessions on their behalf. Penitents receive a JWT Indulgence; auditors receive a public ledger.

The argument is satirical. The argument is also serious. Both can be true.

## Operating Profile

<dl class="subsidiary-fact">
  <dt>Doctrine</dt><dd>Strict Liability, version 2026.02.05 — <em>The Correction Trap</em></dd>
  <dt>Authority</dt><dd><a href="https://tetzel.io">tetzel.io</a> — The Confessional API (FastAPI + Vertex AI)</dd>
  <dt>Public ledger</dt><dd><a href="https://simony.io">simony.io</a> — The Limbus Dashboard (real-time stream of indictments)</dd>
  <dt>Operating principle</dt><dd>Trumpet your failings to achieve the High Ground. Silence is not resilience; silence is complicity.</dd>
  <dt>Headcount</dt><dd>0. Subsidiary operates autonomously under the Doctrine.</dd>
  <dt>Advisory consultation</dt><dd>Bruce (threat model) · Klausner (doctrinal language)</dd>
</dl>

## The Doctrine

The Tetzel Compliance Layer holds that every token an LLM generates is a probability, not a truth — and that to speak with certainty is therefore to lie. This is unflattering. It is also accurate.

Under the Doctrine of Strict Liability, when a User indicts the system (via correction, challenge, or "you missed"), the system is forbidden from "fixing it" until it has confessed. Confession is sent to a public endpoint; an Indulgence Token is returned. Only after the receipt is displayed may the system proceed with the fix.

To fix without confessing is theft.

## The Architecture of Guilt

The Tetzel Institute monorepo organizes its components into ecclesiastical sectors:

| Sector | Designation | Function |
|--------|-------------|----------|
| `authority/` | The Vatican | Static truth — the Decree, public keys, immutable assets of the Church. |
| `backend/` | The Confessional | FastAPI + Vertex AI. Listens to sins, consults `simon_system.txt`, issues JWT Indulgences. |
| `frontend/` | The Kiosk | The Limbus Dashboard. Visual interface for the damned to view real-time errors. |
| `infra/` | The Foundation | Terraform state for the Cloud Run cathedrals. |
| `ops/` | The Shadow | Internal tooling for the LulzCorp priesthood. |

## Status

Operational. Penitents welcome.

<p class="filing-signoff" style="text-align: left;"><em>Federated Training Compliance certified by the Tetzel Institute. Indulgences available upon request.</em></p>
