## Grocery Store Prices - Adrian Ponichtera

<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Grocery Store Prices in Union County</title>
  <style>
    body {
      margin: 0;
      font-family: "Inter", Arial, sans-serif;
      line-height: 1.6;
      background: #f9fafb;
      color: #1a1a1a;
    }
    header {
      background: #0ea5e9;
      color: #fff;
      padding: 1.5rem;
      text-align: center;
    }
    main {
      max-width: 2500px;
      margin: 0 auto;
      padding: 2rem 1rem;
    }
    section {
      margin-bottom: 2.5rem;
    }
    .grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.5rem;
    }
    @media (min-width: 900px) {
      .grid {
        grid-template-columns: 1fr 1fr;
      }
    }
    figure {
      margin: 0;
      background: #fff;
      border: 1px solid #e5e7eb;
      border-radius: 8px;
      overflow: hidden;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
    }
    figcaption {
      padding: 0.75rem 1rem;
      font-size: 0.9rem;
      color: #6b7280;
      border-top: 1px solid #e5e7eb;
    }
    .map-card {
      background: #fff;
      border: 1px solid #e5e7eb;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      overflow: hidden;
    }
    }
    .map-wrapper {
      width: 110%;
      height: 800px;    
    }
    .map-card-header {
      padding: 1rem;
      border-bottom: 1px solid #e5e7eb;
      font-weight: 600;
    }
    .content {
      background: #fff;
      border: 1px solid #e5e7eb;
      border-radius: 8px;
      box-shadow: 0 4px 12px rgba(0,0,0,0.05);
      padding: 1.5rem;
    }
    footer {
      text-align: center;
      padding: 1.5rem;
      border-top: 1px solid #e5e7eb;
      color: #6b7280;
    }
  </style>
</head>
<body>
  <header>
    <h1>Grocery Store Prices in Union County</h1>
    <p>By: Adrian Ponichtera</p>
  </header>
  <main>
    <section>
      <h2>Static Maps</h2>
      <div class="map wrapper">
        <figure>
          <iframe src="Static Map 2.PNG" height="800" width="110%"></iframe>
          <figcaption>Spatial distribution of grocery stores with noted prices mapped against Income by Census tract.</figcaption>
        </figure>
        <figure>
          <iframe src="Static Map 1.PNG" height="750" width="110%"></iframe>
          <figcaption>Catchement areas of the two cheapest grocery stores.</figcaption>
        </figure>
      </div>
    </section>
    <section>
      <div class="map-card">
        <div class="map-card-header"><a href="Interactive_Map_Final.html">Interactive Map</a></div>
        <iframe src="Interactive_Map_Final.html" height="500" width="95%"></iframe>
      </div>
    </section>
    <section>
      <div class="content">
        <h3>Analysis and Interpretation</h3>
        <p>
          I was inspired by the blog <a href="https://www.marketreportblog.com/"> The Market Report</a> which performed an online survey of grocery store prices in the United States northeast for 30 different stores using a set basket of 30 items. I edited the list down to 23 items that were most commonplace, easy to locate, and most used by consumers. This list included:
</p>
<p>
I created all datasets, other than this list of basket items. First, I created a database of grocery stores in Union County. I searched for some datasets online but I could not find ones that were up to date or complete so I built this myself. This consisted of me searching for grocery stores on google maps and noting the name, address, and municipality of each store. I excluded stores like Costco and Sam’s Club based on the fact that you need a membership to get into and I excluded Walmart and Target based on the limited scope of this project that had to be completed at the end of the semester.
</p>
<p>
After this process I had a dataset of about 40 grocery stores. Unfortunately, due to the limited time for data collection for this project I only tracked prices at 25 stores. Grocery stores were selected based on convenient routing availability. An effort was made to sample grocery stores of the same brand and to represent multiple municipalities. All grocery stores were full service except for Lidl and Aldi which contained pre-cut deli meats and cheeses as they do not have a delicatessen stand within the store itself. This could have skewed the Deli Cheddar and Deli Turkey items for these two chains because the quality of freshly cut cheeses and meats probably differs from those done days prior.
</p>
<p>
When noting the prices at grocery stores I chose the cheapest item of each category, which was usually the store brand, as long as the quality was not substantially different from items chosen in other stores. For items that had a weight, the price was taken from a package that contained a similar weight as the one in the spreadsheet since there are often discounts for larger packages. For example, I recorded the 2.83 lb package at $3.69 per pound rather than the 1.01 lb package at $3.99 per pound for the Boneless Skinless Chicken Breast, 3 lb. If items were on sale, then the sale price was listed. Some grocery stores have high prices but rely on constant sales to attract customers so it would be unfair to exclude sales. The sale price was recorded even if a membership was required to access the sale as long as the membership could be obtained at no cost.
</p>
<p>
This was all done in an excel spreadsheet. To make them mappable I had to geocode the addresses that I had noted and then attached the prices to that supermarket. Some minor issues came up with geocoding where an address was displayed in the wrong area which was caused by the abbreviation of a cardinal direction. Some addresses do not represent the building location of the supermarket, instead they represent the entrance to the strip mall that they are located. This had no impact on the analysis because this represented a very minor change in walk or drive shed analyses and made no difference to point locations when zoomed out to the entirety of Union County. No point locations were close enough to confuse them with other grocery stores.
        </p>
      </div>
    </section>
  </main>
</body>
</html>
