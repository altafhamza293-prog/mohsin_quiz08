# step 1 next.js folder
first we open window then type cmd
after cmd open we type cd desktop 
then npx create-next-app@latest my name
mohsin.nextjs
cd mohsin.nextjs
npm install@supabase/supabase.js
npm run dev

# step 2
Supabase → stores and manages database data.
Connection → Next.js connects to Supabase using Supabase’s client library.
You can add, read, update, and delete data from Supabase in your Next.js app.
Example: login system, products, users, notes, or orders.

# step 3
import { createClient } from '@supabase/supabase-js'

const supabase = createClient(
  'YOUR_SUPABASE_URL',
  'YOUR_SUPABASE_ANON_KEY'
)

export default supabase

# step 4
import { createClient } from '@supabase/supabase-js'

export const supabase = createClient(
  process.env.NEXT_PUBLIC_SUPABASE_URL,
  process.env.NEXT_PUBLIC_SUPABASE_ANON_KEY
)
import { supabase } from '../lib/supabase'

export default function Home() {
  return <h1>Next.js + Supabase Connected</h1>
}