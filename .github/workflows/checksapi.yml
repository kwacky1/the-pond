name: Checks API

on:
  push
jobs:
  check-code:
    runs-on: ubuntu-latest
    steps:
      - name: Checks API
        run: |
          curl --request POST \
          --url https://api.github.com/repos/${{ github.repository }}/check-runs \
          --header 'authorization: Bearer ${{ secrets.GITHUB_TOKEN }}' \
          --header 'accept: application/vnd.github.antiope-preview' \
          --data '{
          "name": "code-coverage",
          "head-sha": "ed74cde7c5610864ff8307bdc2c60e126629ba61",
          "status": "in_progress",
          "output": {
              "title": "Check me out baby",
              "summary": "",
              "text": ""
          }'
