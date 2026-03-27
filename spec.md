# Airu — Early Access

## Current State
- Hero section has inline WaitlistForm component with form fields
- WaitlistModal exists but is triggered separately by header button
- Solution section shows airflow graphic image
- CTAs say "Join Early Access" across the site
- No sticky bottom CTA bar
- Social links use old Instagram/YouTube handles
- Final CTA section uses inline WaitlistForm
- No video placeholder anywhere

## Requested Changes (Diff)

### Add
- Popup modal replaces ALL inline forms (hero and final CTA sections both use the modal)
- Video placeholder in solution section: dark frame, rounded corners, play button, "See how Airu works in a real room" overlay, clicking shows a "Coming Soon" tooltip/message
- Sticky bottom bar (mobile + desktop): "Limited first batch available" text + "Pre-order" button that opens the popup modal
- Trust indicators scattered across page: "Tested in real Indian homes", "Designed for closed AC rooms", "Built for everyday use"

### Modify
- Hero section: remove inline WaitlistForm entirely; replace with single CTA button "Pre-order Early Access" that opens popup modal; add subtext "No payment required • Limited first batch" below button
- All CTA buttons sitewide → "Pre-order Early Access" (navbar button, hero, final CTA)
- WaitlistModal button text: change "Join Early Access" → "Reserve My Spot"
- WaitlistModal trust text: update to "No payment required. We'll contact you before launch."
- Solution section: replace airflow image with premium video placeholder frame
- Final CTA section: remove WaitlistForm; headline → "Be among the first to experience better air."; subtext → "Limited first batch. No upfront payment."; add single CTA button "Pre-order Early Access" that opens popup modal
- Instagram link: update to https://instagram.com/breathefreshair.india everywhere
- YouTube link: update to https://youtube.com/@BreatheFreshAir everywhere
- Social section handle text: update to match new handles
- Visual polish: increase section spacing, smoother animations, more black/white/beige contrast

### Remove
- WaitlistForm component usage from hero section
- WaitlistForm component usage from final CTA section
- Inline form in hero replaced by modal trigger button

## Implementation Plan
1. Update WaitlistModal: change submit button text to "Reserve My Spot", update trust text
2. Update Header: change button text to "Pre-order Early Access", update social links to new handles
3. Update LandingPage:
   - Hero: remove WaitlistForm, add single CTA button opening modal, add subtext below
   - Solution section: replace airflow image with video placeholder (dark overlay, play icon, coming soon on click)
   - Final CTA: remove WaitlistForm, update headline/subtext, add CTA button opening modal
   - Update all Instagram/YouTube links throughout
   - Add sticky bottom CTA bar component
   - Add "How It Feels" section after "How It Works"
   - Add trust indicators scattered across relevant sections
   - Update social section handles
4. Delete or stop using WaitlistForm component from hero/final CTA (keep it in case admin uses it elsewhere, but remove from landing page)
