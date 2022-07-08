docker run --rm -it -v $(pwd):/app/docs mdtest:latest docs
docs/test.md:4 MD031/blanks-around-fences Fenced code blocks should be surrounded by blank lines [Context: "```shell"]
docs/test.md:6 MD031/blanks-around-fences Fenced code blocks should be surrounded by blank lines [Context: "```"]

---

docker run --rm -it -v $(pwd):/app/docs mdtest:latest .        
docs/README.md:1 MD041/first-line-heading/first-line-h1 First line in a file should be a top-level heading [Context: "docker run --rm -it -v $(pwd):..."]
docs/README.md:2:81 MD013/line-length Line length [Expected: 80; Actual: 118]
docs/README.md:3:81 MD013/line-length Line length [Expected: 80; Actual: 113]
docs/test.md:4 MD031/blanks-around-fences Fenced code blocks should be surrounded by blank lines [Context: "```shell"]
docs/test.md:6 MD031/blanks-around-fences Fenced code blocks should be surrounded by blank lines [Context: "```"]