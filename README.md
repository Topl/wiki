# Topl Wiki

This project makes use of the mkdocs framework to generate the Topl public wiki.

## Testing the project locally

When writing documents, it can be useful to preview what the site will look like without committing the changes. To do so, follow these steps:

1. Clone the repository to your local machine: `git clone https://github.com/Topl/wiki`
2. Navigate to the folder: `cd wiki`
3. Create a new Python virtual environment: `python -m venv venv`
4. Activate the newly-created virtual environment: `source venv/bin/activate`
5. Install the required python dependencies: `pip install --upgrade -r requirements.txt`
6. Run the MkDocs engine: `mkdocs serve`
7. You can now view a preview of the site in your browser at [http://127.0.0.1:8000/](http://127.0.0.1:8000/)

## Adding new pages

The organizational layout of the site is controlled by the `mkdocs.yml` file. The hierarchy is as follows:

```
nav:
  - 'Nav-Bar Entry'
    - 'Sidebar Entry'
      - 'Subgroup Entry'
```

There is one additional layer of organization applied; the Markdown section headers appear below their document title in the sidebar.
This allows readers to jump directly to a subsection within a file if desired.

*Note: All content that should be displayed must be placed in the `docs` subfolder.*

## Deploying the site

All changes which are merged into `main` will automatically be built and published via GitHub Actions integration. To avoid merge conflicts,
creating "topic" branches and merging them via a pull request is preferred.
