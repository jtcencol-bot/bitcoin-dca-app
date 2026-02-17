# Before / After Snapshot — Web3 + Security + Chart Refinement

## Compare Range
- **Before:** `73eb877` (pre-Web3 visual/chart evolution)
- **After:** `310ecc3` (post Sentinel hardening + chart v3)
- **GitHub diff:** https://github.com/jtcencol-bot/bitcoin-dca-app/compare/73eb877...310ecc3

## What changed since before state

### UX / Visual
- Mobile quick-jump nav and sticky action bar.
- Collapsible mobile sections.
- Web3-style visual skin (glow/depth/glass-like cards).

### Functional
- Added optional DCA end date + ongoing toggle.
- Sell-aware simplified modeling integrated into summary/flow.
- Chart upgraded to **Invested vs PnL** with sign-aware PnL color and BTC/ETH normalized overlays.

### Security / Reliability (Sentinel follow-up)
- Added date clamp guard for old anomalous ranges (`>= 2010-01-01`).
- Optimized chart data computation from nested historical recompute to single-pass accumulation.
- Removed raw Shakepay CSV persistence from localStorage (session memory only).

## Feature Delta (postable)
1. App now feels mobile-first and significantly cleaner to use.
2. Added richer, more meaningful performance visualization (Invested vs PnL).
3. Improved safety posture (range clamp, compute hardening, reduced local privacy exposure).
4. Maintained browser-local privacy model (no backend required).

## Revert quick options
- Revert latest hardening commit only:
  ```bash
  cd /Users/jt/.openclaw/workspace-main/bitcoin-dca-app
  git revert 310ecc3
  git push
  ```
- Return to pre-web3 baseline tag:
  ```bash
  git checkout pre-web3-skin-20260216-1857
  ```
