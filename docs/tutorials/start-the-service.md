
# Start the Furniture Style Sleuth Service

After setting up your environment, follow these steps to start the local server and test that it’s running correctly.

## Step 1: Start the Service

1. Clone your fork and check out a test branch:

    ```bash
    git clone https://github.com/YOUR-USERNAME/furniture-style-sleuth-docs.git
    cd furniture-style-sleuth-docs
    git checkout -b tutorial-test
    cd api
    ```

2. Run the service:

    ```bash
    json-server -w furniture-db.json
    ```

You should see output like:

```
{^_^}/ hi!

Loading furniture-db.json
Done

Resources:
http://localhost:3000/furniture
http://localhost:3000/styles
```

## Step 2: Test the Service

Make a test call:

```bash
curl http://localhost:3000/furniture
```

You should receive a JSON response like:

```
[
  {
    "id": 1,
    "name": "Eames Lounge Chair",
    "style_id": 1,
    "material": "Plywood, leather"
  }
]
```

## Troubleshooting
If you encounter errors:

* Double-check the command syntax

* Ensure you’re in the correct directory

* Confirm that all software is properly installed and up to date

If you get a successful response, you’re ready to begin the [Tutorials](../tutorials/tutorial-find-furniture-by-style.md). 