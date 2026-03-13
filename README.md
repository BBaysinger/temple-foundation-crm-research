# Temple Foundation CRM Research

## Overview

Temple Foundation (working name) is an early-stage nonprofit in Spokane, Washington focused on wellbeing through spirituality, personal growth, and community connection. This repository tracks the CRM selection process to support event coordination, donor management, communications, and long-term operational growth.

The project goal is to identify a CRM that is affordable now, practical for a small team, and scalable as organizational needs evolve.

## Current Context

- Early-stage nonprofit with limited administrative staff
- Cost-sensitive target budget: $150/month
- Strong near-term need for event and community engagement tools
- Website platform not yet finalized
- Long-term need for clean website integration and low maintenance overhead

## CRM Selection Goals

The selected CRM should:

1. Meet current operational needs
2. Stay cost-effective within budget constraints
3. Scale with growth
4. Integrate with future website architecture
5. Minimize long-term technical burden

## Repository Structure

- [README.md](README.md): project context, goals, and navigation
- [requirements.md](requirements.md): known and validated requirements for Temple Foundation
- [common-crm-features.md](common-crm-features.md): broad feature inventory for current and future-state planning
- [non-profit-crms-list.md](non-profit-crms-list.md): shortlist of candidate CRM platforms
- [composable_nonprofit_stack.md](composable_nonprofit_stack.md): modern website-as-platform architecture option and rollout guidance
- [supabase_nonprofit_platform.md](supabase_nonprofit_platform.md): Supabase-first backend architecture for donations, memberships, events, and volunteers
- [evaluation-matrix.md](evaluation-matrix.md): side-by-side scoring and final recommendation inputs
- [implementation-style-matrix.md](implementation-style-matrix.md): implementation and styling options matrix (headless/templates/widgets/CSS control)
- [crm-form-inclusion-evaluation.md](crm-form-inclusion-evaluation.md): CRM-by-CRM comparison of form inclusion modes, website control, and setup tradeoffs
- [crm-exit-migration-notes.md](crm-exit-migration-notes.md): preliminary assessment of how difficult it would be to migrate away from each shortlisted CRM later
- [nonprofit-saas-crm-growth-migration-notes.md](nonprofit-saas-crm-growth-migration-notes.md): overview of how often nonprofits outgrow SaaS CRMs, what drives replatforming, and what warning signs to watch for
- [temple-foundation-civicrm-evaluation-notes-2026-03-13.md](temple-foundation-civicrm-evaluation-notes-2026-03-13.md): focused notes on CiviCRM fit, rollout risk, and support implications for Temple Foundation

## Time Estimate Docs

- [time-estimate-docs/civicrm-solo-independent-gpt.md](time-estimate-docs/civicrm-solo-independent-gpt.md): solo CiviCRM implementation timeline (GPT version)
- [time-estimate-docs/civicrm-solo-independent-codex.md](time-estimate-docs/civicrm-solo-independent-codex.md): solo CiviCRM implementation timeline (Codex version)
- [time-estimate-docs/civicrm-wordpress-setup.md](time-estimate-docs/civicrm-wordpress-setup.md): phased setup steps and timeline estimates for CiviCRM + WordPress
- [time-estimate-docs/required-items-difficulty-time-template-for-claude.md](time-estimate-docs/required-items-difficulty-time-template-for-claude.md): Claude-authored required-item difficulty ranking and effort estimates from the evaluation matrix
- [time-estimate-docs/required-items-difficulty-time-gpt.md](time-estimate-docs/required-items-difficulty-time-gpt.md): GPT-authored required-item difficulty ranking and effort estimates from the evaluation matrix
- [time-estimate-docs/required-items-difficulty-time-codex.md](time-estimate-docs/required-items-difficulty-time-codex.md): Codex-authored required-item difficulty ranking and effort estimates from the evaluation matrix
- [time-estimate-docs/required-items-difficulty-time-gpt-optimistic.md](time-estimate-docs/required-items-difficulty-time-gpt-optimistic.md): more optimistic GPT estimate variant for the required-item implementation scope
- [time-estimate-docs/required-items-difficulty-time-codex-optimistic.md](time-estimate-docs/required-items-difficulty-time-codex-optimistic.md): more optimistic Codex estimate variant for the required-item implementation scope
- [time-estimate-docs/line-by-line-estimate-comparison.md](time-estimate-docs/line-by-line-estimate-comparison.md): side-by-side line-item effort comparison across Codex, GPT, Pipedrive, Neon CRM, and Givebutter + Bloomerang

## Evaluation Workflow

1. Define validated requirements
2. Build a candidate CRM shortlist
3. Score options against weighted criteria
4. Document tradeoffs, risks, and recommendation rationale
