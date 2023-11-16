## node-backend

- A `express` backend only app which can be used as starter for any backend or suitable frontend.
- It is running as a set of 2 docker containers: `backend` and `postgres`.
- Backend contains only one table `post` which is used to query/persist the data.
- Seed data is already available in app itself and with `docker:db:migrate` it is pushed to db.
- Only one endpoint, root as `'/'` is there to query the data.

### tech involved

- `prisma` for type generation
- `knex` for db migration (here table generation)
- `swc` for transpiling typescript
- `docker` to run containers

### scripts

- `build` for prod build
- `start` to start in dev mode
- `db:console` to look into and query postgres
- `rebuild:be` only rebuild backend, if made any changes or install/change new deps
- `docker:db:migrate` to generate db structure (table) in db
- `build:prisma` to generate typescript types to further facilitate development
