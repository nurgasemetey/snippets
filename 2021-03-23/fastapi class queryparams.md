### fastapi class queryparams


[\[QUESTION\] Using pydantic models for GET request query params? Currently not possible, have to use dataclasses or normal classes. · Issue #318 · tiangolo/fastapi](https://github.com/tiangolo/fastapi/issues/318 "[QUESTION] Using pydantic models for GET request query params? Currently not possible, have to use dataclasses or normal classes. · Issue #318 · tiangolo/fastapi")


 

```
app = FastAPI()


class SearchArgs:
    def __init__(
        self,
        query: str = Query(...),
        limit: int = Query(10),
        offset: int = Query(0),
        sort: str = Query("date"),
    ):
        self.query = query
        self.limit = limit
        self.offset = offset
        self.sort = sort


@app.get("/api/v1/search_dataclass", tags=["basic"])
def search(args: SearchArgs = Depends()):
    return {"detail": "search-result", "args": args, "results": {"abc": "def"}}
```
