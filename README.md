#Media and Typography Optimization Build

3. Reasoning for Not Using Art Direction (no <picture>)

I do not currently need <picture> for art direction because the same square compositions work at both narrow and wide layouts. The headshot remains centered and recognizable when resized, while the project thumbnails were designed as square portfolio graphics.

Therefore, srcset is being used for resolution switching, not art direction. The browser can choose a smaller or larger version of the same composition.

If a future hero layout requires a tighter portrait crop on narrow screens and a wider environmental image on desktop, I could then use <picture> to provide different compositions.



5. As of right now SVGs, audio, video, animation, and embeds are not currently planned to be implemented onto the website


9. Testing Evidence

Test	                    What to verify

Narrow viewport	            Images resize without overflow; hero stacks; cards remain readable.

Medium viewport	            Hero changes to its two-column layout when enough space is available.

Wide viewport	            Content remains constrained and images do not become unnecessarily large.

200% zoom	                Text and cards reflow without clipping, overlap, or page-level horizontal scrolling.

Slow network	            Fallback font appears while Commissioner loads; reserved image regions prevent major movement.

Image dimensions	         Confirm exported 320/640 variants have the expected pixel dimensions.

File size	                 Compare image file sizes and compress oversized assets.

srcset	                     Use browser developer tools to confirm appropriate image candidates load.

Alt text	                 Inspect every <img> and verify informative images have useful alternatives and redundant/decorative images use alt="".

Reduced motion	             Enable prefers-reduced-motion: reduce and confirm card movement/transitions stop.

Keyboard	                Tab through navigation and clickable cards and confirm visible focus indicators.

Layout shift	            Verified that images do not cause major content jumps.

Captions/transcripts	    Not applicable currently because the site does not contain audio or video.


10. AI Disclaimer

    I used AI for mostly size recommendations when it came to the images for the srcset, sizes (the attribute), and the width and height of the images. Other than that, everything else was done by myself.