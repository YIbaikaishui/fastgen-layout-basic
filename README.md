# FastAPI Basic Layout (fastgen)

A minimal `src/`-layout FastAPI project — nothing you didn't ask for. This is
fastgen's **basic layout**: config, database, health endpoint, tests, Alembic,
and an empty module registry waiting for your first feature.

## Quick start

```bash
uv sync
uv run alembic upgrade head
uv run uvicorn src.main:app --reload     # http://localhost:8000/docs
uv run pytest
```

## Add modules

```bash
uvx fastgen-cli make module order
```

That creates `src/modules/order/` (domain / application / infrastructure / api /
tests), registers it, and its router is served automatically — `main.py` is
never hand-edited. See the module map anytime with `uvx fastgen-cli list`.

## Other layouts

- **advanced** — the same structure with a worked CRUD example:
  https://github.com/YIbaikaishui/fastgen-layout-advanced

## License

MIT
