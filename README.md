# Case Study on Dubai Flash floods (April 17, 2024) - How to detect floods using Satellite Imagery

This article is a case study covering geospatial analysis of Dubai flooding using extensive use of satellite imagery tools.

Very recently the world woke up to the news about Dubai Airport getting flooded due to a rare storm (more than 250 mm of rainfall in 24 hours!!). This created an opportunity for Geospatial Data Science enthusiasts to get going in the pursuit of finding the reason behind this flash flooding in a desert land. 

In this scenario, clear satellite images are the most critical data resource, and we need to demonstrate a simple method of separating flooded and non-flooded areas. Luckily, Sentinel-2 captured two images on April 7th (pre-flood event) and 17th (post-flood event), mostly free of clouds over Dubai. Those images led to this analysis and case study, explaining how to detect flood events using satellite images.

--Technical brief--

1. In this article, we kick off by utilizing a Python script to fetch Sentinel-2 imagery of a flooded area in Dubai. 
2. Next, employing the rasterio package, we'll decode the imagery and calculate the Normalized Difference Water Index (NDWI) by leveraging near-infrared and green bands. 
3. Subsequently, we'll generate histograms of NDWI for both pre and post-flood images. 
4. By juxtaposing these histograms, we can discern the transformation of dry regions in the pre-flood image into inundated areas in the post-flood image. 
5. Ultimately, employing a threshold derived from the histogram analysis, we'll isolate the flooded pixels and delineate the submerged zones on a map.

If this piques your interest, continue reading for more insights!


# Table of Contents

🌅 Introduction
💾 Downloading Sentinel-2 Imagery
⚙️ Clipping and Stacking Multispectral Bands
📐 Calculation of NDWI
📊 NDWI Histogram
🗺️ Visualization of Flooded Areas
📄 Conclusion
📚 References
