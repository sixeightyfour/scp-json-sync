# Daily Updated SCP Data

Publicly available site scrape of the SCP Wiki, updated daily at 5:30 UTC. Trimmed to contain the data most likely needed for data analysis or visualization, with additional data available.

## Data Provided

### Merged Data:

The following data is bundled together for all pages of each type (`goi.json`, `scp_hubs.json`, `scp_items.json` and `scp_tales.json`) in JSONs located in the `raw/` folder:
* `url`: Full URL for the page (scp-wiki.wikidot.com/scp-xxxx).
* `link`: Page slug (scp-xxxx).
* `rating`: Page rating at the time of the scrape.
* `tags`: All tags associated with the page.
* `references`: Outbound hyperlinks found on the page.
* `title`: Page title.

Articles in `scp_items` also contain the following:
* `series`: Series the article belongs to (series-9).
* `scp`: String containing "SCP-XXXX".
* `scp_number`: Integer containing the article number (XXXX).

The data above is also available as a single file (`merged/all_pages.json`).

### Split Data:

Edit history gathered from the scrape has potential use cases, but is otherwise very bulky. I have provided this data as separate JSONs located in the `split/` folder, so that they may be pulled only if required.

This includes:
* `created_at`: Date of page creation.
* `creator`: Wikidot account that created the page.
* `history`: Edit history for the page, containing:
  *  Editor account (`author`),
  *  The corresponding Wikidot user page (`author_href`),
  *  Any comment the author might have made about their changes (`comment`),
  *  The date and time of the edit (`date`).

## Attribution:

This work was made possible using the [scp-crawler repository](https://github.com/scp-data/scp_crawler). This data is freely available for use with attribution under the Creative Commons 3.0 ShareAlike License.
