# Comparison of Grind Sizes

Repo of personally collected data using [coffeegrindsize app](https://github.com/jgagneastro/coffeegrindsize), BUT [using this forked repo](https://github.com/wannabecoffeenerd/coffeegrindsize) which has the addition of 4/3 factor for volume calculation from [wannabecoffeenerd's unmerged pull request](https://github.com/jgagneastro/coffeegrindsize/pull/11). So yes, these will be differnt results than from others in [this fledgling ground database](https://github.com/Coffee-Grind-Distribution/coffee-grind-distribution) but they will at least be self-consistent.

First goal is to compare consistency of grind size form the Hario Mini grinder varying inclusion of bottom axis stabilizer and as-is vs cleaned. (Burrs have not been cleaned since I bought it in 2014 {'now' is 2023}) Grind size i.e. clicks on grinder will stay the same. Large grind size I believe will have more variability than the smaller grind size I would actually want for espresso.

Second goal is to calibrate hario grinder as close to professional grinder & grind settings for espresso as possible. Using grounds that Milstead Coffee gave for the cause. Will update with grinder name & model later.

## Repository Structure

Naming of files in below directories is detailed in each sample section below.
[source-images](source-images) contains the images I have taken of coffee grounds spread out across a page of paper.
[data-outputs](data-outputs) contains the csv files that the coffeegrindsize app saves data to. 
[histogram-images](histogram-images) contains histograms created by coffeegrindsize app. Some have comparison data overlaid as a blue outline. Labels on the histogram are hopefully clear enough.

## Summary Table

| Description         | Avg Diam (mm) | SD Diam | Avg Surface (mm<sup>2</sup>) | SD Surface | Efficiency | Quality |
| ------------------- | ---- | ---- | --- | ---- | ---- | ---- |
| Hario, No Cleaning, Axis Stabilized, Sample 1 Subsample 1 | 1.55 | 0.89 | 2.5 | 2.73 | 87.3 | 0.91 |
| Hario, No Cleaning, Axis Stabilized, Sample 1 Subsample 1, Same Grounds on Paper Just spread out better | 1.13 | 0.62 | 1.3 | 1.44 | 87.7 | 0.9 |
| Hario, No Cleaning, Axis Stabilized, Sample 1 Subsample 2 | 1.62 | 1.02 | 2.88 | 3.54 | 84.8 | 0.82 |
| Hario, No Cleaning, Axis Stabilized, Sample 1 Subsample 2, Sub-subsample 1 | 1.16 | 0.73 | 1.47 | 1.94 | 88.5 | 0.76 |
| Hario, Air Cleaning, Axis Stabilized, Sample 1 | 0.82 | 0.37 | 0.64 | 0.54 | 87.7 | 1.18 |
| Hario, Air Cleaning, Axis Stabilized, Sample 2 | 1.05 | 0.51 | 1.08 | 1.1 | 81.2 | 0.98 |
| Hario, Air Cleaning, Axis Stabilized, Sample 3 | 1.09 | 0.57 | 1.2 | 1.27 | 81.6 | 0.94 |
| Hario, Air Cleaning, Axis Stabilized, Sample 4 | 1.14 | 0.62 | 1.32 | 1.6 | 78.7 | 0.82 |
| Milstead, Sample 1 | 0.8 | 0.36 | 0.6 | 0.56 | 85.0 | 1.08 |
| Milstead, Sample 1 - Spread out more | 0.73 | 0.3 | 0.49 | 0.39 | 85.3 | 1.26 |
| Milstead, Sample 2 | 0.67 | 0.28 | 0.41 | 0.32 | 89.3 | 1.26 |
| Milstead, Sample 3 | 0.78 | 0.34 | 0.58 | 0.48 | 86.6 | 1.19 |


[From manual](https://github.com/wannabecoffeenerd/coffeegrindsize/blob/fd361b02d4b1d4c21e000a2e292ed9f89cecbaee/Help/coffee_grind_size_manual.pdf): The “Quality” number is simply the standard deviation of surfaces divided by the average surface: this number tracks the narrowness of the distribution, and should be a decent indicator of your grinder quality. The “Efficiency” is simply the mass fraction of coffee that is available for extraction by diffusion (please see discussion above about available mass).


## Hario First Sample

Added 3d printed axis stabilizer to Hario Mini grinder, but did not clean it and ground way too many beans from old (but unopened) bag I had.

### First Subsample

From large pile of grounds I took less than a tsp and spread out on paper to get `hario-noCleaning-axisStabilizer-1.jpg` as my first attempt, but many of the grounds were bunched up together. I did not remove or add any grounds, and I believe still captured all the same particles in the image for `hario-noCleaning-axisStabilizer-1-sameGrinds.jpg` Comparison histogram is `hario-noCleaning-axisStabilizer-grind-spread-out-on-paper-more_hist_av_mass_surf.png`

### Second Subsample

From same large pile of grounds I took another less than tsp amount and spread out. Apprently I really head spreading out coffee grounds as I got higher results than expected. Image is `hario-noCleaning-axisStabilizer-2.jpg` and histogram with this data compared to `hario-noCleaning-axisStabilizer-1-sameGrinds.jpg` is at `hario-noCleaning-axisStabilizer-2-vs-1_hist_av_mass_surf.png`

#### Subsample of Second Subsample

Threw maybe 3/4 of grounds off the paper from `hario-noCleaning-axisStabilizer-2.jpg` and spread out the remainders to get `hario-noCleaning-axisStabilizer-2-subsample1.jpg`. Histogram `hario-noCleaning-axisStabilizer-2-subsample1-vs-Sample1hist_av_mass_surf.png` is a comparison of this Sub-subsample of Subsample 2 vs Subsample 1 with ground better spread out.

Histogram `hario-noCleaning-axisStabilizer-2-subsample1-vs-Sample2-hist_av_mass_surf.png` is a comparison of this Sub-subsample of Subsample 2 vs Subsample 2 (e.g. before grounds were removed to make the Sub-subsample). This comparison shows that a lot of the bigger particles in Subsample 2 are likely 2 or more grounds sitting next to each other. Alternatively I may have just removed more of the larger particles with my 'get these darn grounds off the paper' "method" of creating the sub-subsample.


## Hario Cleaned with Compressed Air, First Sample

Hario was cleaned quickly using compressed air from top and bottom of burrs. Then I ground 20g of same old house beans. Main reason was to have something to run water through picopresso for the first time to clean/flush it. Made more than needed so I could run a comparison after using compressed air to blow out fine particles in burrs.

Source image is `hario-airClean-axisStabilizer-sample1.jpg`. Results added to summary table above and comparison of Hario No Cleaning vs Hario Air Cleaning is at `hario-airClean-axisStabilizer-sample1-vs-noCleaning-1-sameGrinds-hist_av_mass_diam.png`

Looking at results table, I expected a much bigger difference between professional ground and these. The comparison of the shots was completely different. The beans were old but it was much easier to pump water through the picopresso/grounds with the hario ground beans... Ugh this makes me want to do another sample from the milstead pile of grounds to see if I get similar results. Though looking again the average diameter may not be a large difference, hario does have many more large particles than the professional grounds.

## Hario Cleaned with Compressed Air, Second Sample

I cleared out previous grounds from burrs using compressed air, from top and bottom. Then placed one bean in the hopper and ground while grinder was flat on the piece of paper, no grounds catcher screwed on. Then spread out the grounds.

Comparison of this data to Sample 1 shows this sample has appreciably more large particles and a higher average diameter. Not sure whwy. Maybe I didn't spread them out as much, again?? This isn't doing much for my faith in reproducing results :-/

## Hario Cleaned with Compressed Air, Third Sample

Again, I cleared out previous grounds from burrs using compressed air, from top and bottom. Then placed one bean in the hopper, but this time I ground while grinder was about 50mm above the piece of paper, no grounds catcher screwed on. I moved the grinder around the paper as I went, and this time I spent far less time spreading out the grounds after I was done grinding.

Results were similar to the Second Sample. Ok maybe a little repeatable. Sigh, let's do another.

## Hario Cleaned with Compressed Air, Fourth Sample

Again, I cleared out previous grounds from burrs using compressed air, from top and bottom. Then placed one bean in the hopper, but this time I ground while grinder was about 50mm above the piece of paper, no grounds catcher screwed on. I moved the grinder around the paper as I went. This time I spent a little more time than on the third sample spreading out the grounds after I was done grinding.

Results were similar to second and third sample. Ok, somewhat repeatable. Let's move on to getting better grind size on hario so I can actually dirnk espresso instead of pushing grounds around.

## Milstead Professional Ground

Did not get name/model of grinder. Got 19g of beans from Milstead to try in picopresso. And wow the result - from 18g of grounds, 70g of water, outputtung 40g of espresso - was very similar! slightly more muted flavors and sharper with a little sourness at end, but a good shot. Would enjoy if I got it from a coffee shop! But yes, not quite as good as what I just had from Milstead with same beans, grinder, and grind settings.

### Sample 1

Used some of leftover grounds to do paricle analysis. Used less than 1g (i.e. scale did not change) of grounds and took `milstead-sample1-pic1.jpg` and `milstead-sample1-pic2.jpg` at the same time, so did not do analysis on pic2. Looked at particle detection results and went back to paper sheet and tried to spread out any large chunks that proogram identified. Many I coudl spread out, some were just large particles. Then took `milstead-sample1-pic3.jpg`. Saved results and also comparison histograms. Indeed I was able to see a difference with more effort spreading out particles. More fine and significantly less large particles - see `milstead-sample1-pic3-vs-pic1-hist_av_mass_diam.png`. NB: No particles were added or taken away from paper/image. I just spent much more time than I wish poking and sweeping particles apart.

## Sample 2

Then cleaned off sheet of paper and took two pinches of grounds from same milstead ground pile and spread on paper. Trying to use far less grounds to see if I could get similar results to `pic3` - so I coudl spend less time spreading grounds. My pinch 'method' I figured may be better than tapping grounds out of container which had an interior lip - but maybe some fine particles would be stuck on fingers? This resulted in more fine particles and less large particles than sample1-pic3 (sample that was spread out on paper more) - see `milstead-sample2-pic1-vs-sample1-pic3-hist_av_mass_diam.png` Reason? Either I took fewer large particles from pile of grounds that were left, or more had been removed by previous tapping method, or there were just less grounds on the paper so I had more patience to spread them out. I am ok not knowing this for sure right now, they were close. see results table above.

## Sample 3

Took rest of grounds from canister and dumped onto sheet. spread it out. Got larger average diameter than Sample 2 and more large particles. See `milstead-sample3-pic1-vs-sample2-pic1-hist_av_mass_surf.png`. I think this mostly goes to show I am tired of spreading out coffee grounds. Image is in repo if I want to go back later and exclude clusters/clumps and see if I get different results. But not right now.


## Next Tests

Hario Grinder 'cleaned' by using canned air to blow out small particles. Two samples below I assume will be very similar to above Sample #1. Any deviations are more likely from the smaller amount of beans ground (and thus not testing my patience as much to better seperate the grounds on the paper).

- [x] Grind a few beans with axis stabilizer installed
- [ ] Grind a few beans without axis stabilizer installed

Dissasemble Grind and clean ceramic parts well with Baking soda

- [ ] Grind a few beans with axis stabilizer installed
- [ ] Grind a few beans without axis stabilizer installed

Adjust grind size and find what diameter particles come out of the first... 5(?) clicks of grinder
