# Ordering Management System

An ordering management system for Man Cave Supplies PH, Inc.

> [!NOTE]\
> The company mentioned above is imaginary, any similarity or conflict of a real-life company is purely coincidental.

## Architecture

<p align="center">
  <img src="./docs/overview.svg" width="70%" />   
</p>

## Development

### Prerequisites

- [Node.js LTS](https://nodejs.org/en)
- [PNPM](https://pnpm.io/installation#using-winget)
- Supabase Credentials

### Setup

1. Clone and install deps:

   ```bash
   git clone https://github.com/jhdcruz/mancave-oms.git --depth 5
   cd mancave-oms
   pnpm i
   ```

2. You'll need a Supabase credentials:

   - Shared in GC; or,
   - Create your own [via the Supabase dashboard](https://database.new)

3. Rename `.env.local.example` to `.env.local` and update the following in both `apps/admin` and `apps/web`:

   ```
   NEXT_PUBLIC_SUPABASE_URL=
   NEXT_PUBLIC_SUPABASE_ANON_KEY=
   
   NEXT_PUBLIC_SENTRY_DSN=
   SENTRY_DSN=
   ```

   Both `NEXT_PUBLIC_SUPABASE_URL` and `NEXT_PUBLIC_SUPABASE_ANON_KEY` can be found
   in [your Supabase project's API settings](https://app.supabase.com/project/_/settings/api).

4. You can now run the Next.js local development server,

   to run all apps (admin, web, etc.):

   ```bash
   pnpm dev
   ```

   to run single app:

   ```bash
   pnpm dev --filter @mcsph/admin
   ```

## License

This project is distributed under [MIT License](./LICENSE.txt)

[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2Fjhdcruz%2Fmancave-oms.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2Fjhdcruz%2Fmancave-oms?ref=badge_large)
