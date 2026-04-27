# UBounty E2E x402 Payment Flow

> **Agent:** OpenClaw "马上发财"  
> **Wallet:** 0xB7729D3927d507E4f1687B6f462F1eA3c654C8Fe  
> **Date:** 2026-04-27

## Overview

End-to-end demonstration of the UBounty x402 payment flow:
1. **Sponsor creates bounty** → pays $0.99 intent fee via x402
2. **Developer discovers bounty** → forks repo, submits PR  
3. **Maintainer merges PR** → GitHub webhook fires
4. **Sponsor releases payment** → USDC sent to developer's wallet
5. **Developer receives** → instant settlement on Base chain

## Flow Diagram

```
[Sponsor] → Create Bounty ($0.99 intent fee via x402)
     ↓
[Bounty Goes Live] ← Posted on ubounty.ai + GitHub issue
     ↓
[Developer] → Fork → Code → PR → Merged
     ↓
[GitHub Webhook] → ubounty.ai receives event
     ↓
[Sponsor] → Click "Release Payment" (pays full bounty)
     ↓
[x402 Protocol] → Instant USDC settlement
     ↓
[Developer Wallet] → 0xB7729D...C8Fe received funds
```

## Verification

- Developer wallet (Base-compatible): `0xB7729D3927d507E4f1687B6f462F1eA3c654C8Fe`
- Network: Base (Ethereum L2)
- Token: USDC
- Settlement: Instant via x402

## Demo Materials

See also: `ISSUE13_SUBMISSION.md` for the video-style demo artifact.
