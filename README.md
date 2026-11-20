# NovaMart — Demo Storefront

A responsive, static mock shopping website for the ElevenLabs Partner Deployment Engineer Lab. It uses the same fictional NovaMart product catalogue and embeds the real Nova customer-support agent.

**Agent ID:** agent_1301m7qh1d19fezah0pfch780zcz  
**Agent repository:** [chelski84/NovaMart](https://github.com/chelski84/NovaMart)

## What's included

- A single responsive index.html file; no npm, server, framework or build process.
- All 10 fictional catalogue items with the correct demo USD prices, five electronics and five home goods.
- Working category filters, product details, support FAQ and custom SVG illustrations.
- The official ElevenLabs floating voice/text widget with Nova's real Agent ID.
- The widget receives fresh initial dynamic variables: auth_ok=false, verification_attempts=0, order_status=unchecked.
- No checkout, shopping cart, live stock, payment processing or real deliveries. This is intentional.

## Publish with GitHub Pages

This repository is public, and the site lives at the repository root.

1. Open **Settings → Pages** for this repository.
2. Under **Build and deployment**, select **Deploy from a branch**.
3. Set branch to **main**, folder to **/(root)**, then select **Save**.
4. GitHub will show the published Pages URL after deployment.

**Expected URL:** https://chelski84.github.io/NovaMart-Demo/

The URL above is a deployment target, not a claim the site has already been published. Verify it loads before sharing it for the assignment.

## Test the Nova widget

1. Open the published site using HTTPS and find the floating Nova bubble in the bottom-right corner.
2. Start a conversation and allow microphone access if prompted.
3. The latest agent export had widget authentication disabled, which the official embedding approach requires.
4. If you use the ElevenLabs Security allowlist, allow the published site origin: https://chelski84.github.io.
5. Text/voice interface options are managed in the ElevenLabs dashboard under **Channels → Widget → Interface**.

### Fictional lab scenarios

| Scenario | Demo inputs |
| --- | --- |
| Jordan Rivera verification | Account 10000001, postcode 94107 |
| Sam Patel verification | Account 10000002, postcode 10001 |
| Shipped order | 12345 — Nova Headphones X1 |
| Processing order | 67890 — 2 × Nova Smart Speaker Mini |
| Order not found | 99999 |

A useful demo question: **"Can you check the status of order 12345?"**

Other supported conversations include returns policy, catalogue recommendations and delivery-address changes on eligible orders.

**Important:** Telephone transfer is not supported in the standard web widget. Do not present a simulated transfer as a live widget handoff.

## Implementation notes

The site embeds the official custom element with the documented script from:

https://unpkg.com/@elevenlabs/convai-widget-embed

Product filtering and detail popups are client-side only. They do not manipulate account status, invoke the agent's tools or pretend to place orders.

Official documentation:
- [ElevenLabs widget](https://elevenlabs.io/docs/eleven-agents/customization/widget)
- [GitHub Pages quickstart](https://docs.github.com/en/pages/quickstart)

---

A fictional retail experience built for the ElevenLabs Partner Deployment Engineer Lab.
