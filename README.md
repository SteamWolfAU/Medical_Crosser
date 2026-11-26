# Medical_Crosser

**Live app:** https://steamwolfau.github.io/Medical_Crosser/

[![Visits](https://hits.sh/steamwolfau.github.io/Medical_Crosser.svg?label=visits)](https://hits.sh/steamwolfau.github.io/Medical_Crosser/)


A single-file web app. Open `index.html` in any browser, including on a phone. There's no install, no account and no build step, and it works offline.

## What it does

1. **Add your medicines.** Search by generic name (e.g. *atorvastatin*) or Australian brand name (e.g. *Lipitor*, *Nurofen*, *Somac*). Enter the amount each time and how often you take it.
2. **Plain-English side effects for each medicine:**
   - common side effects
   - "get medical help if you notice" warning signs
   - practical tips
3. **Dose check.** Your daily or weekly total is compared with the usual adult range. The app flags doses above the usual maximum, likely mg/mcg mix-ups, and weekly-only medicines (methotrexate) entered as daily.
4. **Combination check** across your whole list, graded *Avoid / Major / Moderate / Minor*:
   - specific known interactions (e.g. nitrates + sildenafil, simvastatin + clarithromycin, warfarin + antibiotics, lithium + NSAIDs)
   - additive effects across any number of medicines: serotonin syndrome, drowsiness and slowed breathing (opioids + sedatives), bleeding, QT/heart rhythm, high potassium, slow heart rate, anticholinergic load, low sodium, low blood pressure, low blood sugar
   - the "triple whammy" (ACE inhibitor/ARB + diuretic + NSAID)
   - two medicines from the same group (e.g. two NSAIDs, two paracetamol products, ACE inhibitor + ARB)
5. **Alternatives available in Australia.** Each medicine lists other brands of the same medicine (generic substitution), plus other medicines in the same group or used for the same purpose. Every list is a reminder to change medicines only with a doctor.
6. **Shared side effects.** A table showing which side effects more than one of your medicines can cause.

7. **Request a missing medicine.** A form opens the user's own email app with a request to medical@bladestar.online ready to send. Nothing is sent automatically.

The list is saved in the browser on that device only. The visit counter at the bottom of the page is an image from hits.sh. It counts page views and receives nothing about the medicines entered. Use **Print / save PDF** to take it to a GP or pharmacist.

## Coverage

There are 120 medicines in total: 109 commonly prescribed and over-the-counter medicines on the Australian market, plus 11 supplements and complementary medicines: fish oil, glucosamine, turmeric, ginkgo, ginseng, valerian, melatonin, magnesium, calcium, iron and St John's wort. These are checked for interactions too, e.g. with blood thinners, or iron/calcium blocking antibiotic and thyroxine absorption. They cover heart and blood pressure, cholesterol, diabetes, stomach, mental health and sleep, ADHD, pain, antibiotics, hormones, bones, gout, blood disorders, skin, allergy, asthma and epilepsy. Search also accepts names as printed on a pharmacy label, e.g. "Bisoprolol Fumarate Tablets 5mg". Medicines that aren't listed can still be added by name. They appear on the printed list but aren't included in the checks.

To add a medicine, add an entry to the `MEDS` array in `index.html`. Use side-effect keys from `SE` and tags that the rules in `PAIRS` / `TAG_RULES` recognise.

## Important

This is general educational information, not medical advice, and it is not exhaustive. The content was compiled from widely known product information. It has **not** been clinically reviewed and doesn't account for age, kidney or liver function, pregnancy or other conditions. Have a pharmacist review the data before relying on it, and always check the Consumer Medicine Information (CMI) leaflet.

## Publishing (GitHub Pages)

The app is a static page with `index.html` in the repository root, so GitHub Pages serves it as-is. The `.nojekyll` file turns off Jekyll processing.

To enable Pages: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**. The site is published at the link above within a minute or two.
