export default function CryptoMillionaireTrackerSite() {
  return (
    <div className="min-h-screen bg-gray-50 text-gray-900">
      {/* Nav */}
      <header className="sticky top-0 z-40 backdrop-blur bg-white/70 border-b">
        <div className="max-w-6xl mx-auto px-4 py-3 flex items-center justify-between">
          <div className="flex items-center gap-2">
            <div className="h-8 w-8 rounded-2xl bg-black" />
            <span className="font-bold tracking-tight">Crypto Millionaire Tracker</span>
          </div>
          <nav className="hidden md:flex items-center gap-6 text-sm">
            <a href="#features" className="hover:opacity-80">Features</a>
            <a href="#demo" className="hover:opacity-80">Live Demo</a>
            <a href="#pricing" className="hover:opacity-80">Pricing</a>
            <a href="#faq" className="hover:opacity-80">FAQ</a>
          </nav>
          <a
            href={GUMROAD_LINK}
            target="_blank"
            rel="noreferrer"
            className="hidden md:inline-flex items-center gap-2 px-4 py-2 rounded-2xl bg-black text-white hover:opacity-90"
          >
            Get the Tracker <ArrowRight className="h-4 w-4" />
          </a>
        </div>
      </header>

      {/* Hero */}
      <section className="relative overflow-hidden">
        <div className="max-w-6xl mx-auto px-4 py-16 grid md:grid-cols-2 gap-10 items-center">
          <div>
            <motion.h1
              initial={{ opacity: 0, y: 10 }}
              animate={{ opacity: 1, y: 0 }}
              transition={{ duration: 0.6 }}
              className="text-4xl md:text-5xl font-extrabold leading-tight"
            >
              See your exact timeline to <span className="inline-block bg-yellow-200 px-2 -rotate-1">$1,000,000</span>
            </motion.h1>
            <p className="mt-4 text-lg text-gray-600">
              A professional Google Sheets dashboard that tracks your portfolio, simulates price targets, and projects
              compounding yield—built for XRP, XDC, ZBC, HBAR, QNT, RNDR and more.
            </p>
            <div className="mt-6 flex flex-wrap items-center gap-3">
              <a
                href={GUMROAD_LINK}
                target="_blank"
                rel="noreferrer"
                className="inline-flex items-center gap-2 px-5 py-3 rounded-2xl bg-black text-white hover:opacity-90"
              >
                Get the Tracker <ArrowRight className="h-4 w-4" />
              </a>
              <a href="#demo" className="inline-flex items-center gap-2 px-5 py-3 rounded-2xl bg-white border hover:bg-gray-100">
                See Live Demo
              </a>
            </div>
            <div className="mt-4 flex items-center gap-4 text-sm text-gray-500">
              <div className="flex items-center gap-1"><ShieldCheck className="h-4 w-4"/> One‑time purchase</div>
              <div className="flex items-center gap-1"><Sparkles className="h-4 w-4"/> 95%+ profit margin</div>
            </div>
          </div>
          <motion.div
            initial={{ opacity: 0, scale: 0.98 }}
            animate={{ opacity: 1, scale: 1 }}
            transition={{ duration: 0.6, delay: 0.1 }}
            className="bg-white rounded-2xl shadow-xl p-4"
          >
            <div className="aspect-video rounded-xl bg-gray-100 overflow-hidden border">
              {/* Replace with a real screenshot */}
              <img
                src="https://images.unsplash.com/photo-1640340434868-3c1c49a5b0e9?q=80&w=1600&auto=format&fit=crop"
                alt="Dashboard preview"
                className="h-full w-full object-cover"
              />
            </div>
            <p className="text-xs text-gray-500 mt-2">Preview of the Portfolio Dashboard</p>
          </motion.div>
        </div>
      </section>

      {/* Social Proof */}
      <section className="py-6">
        <div className="max-w-6xl mx-auto px-4 grid grid-cols-2 md:grid-cols-4 gap-6">
          {[
            { label: "Avg. setup time", value: "5–10 min" },
            { label: "Preloaded tokens", value: "12+" },
            { label: "Dashboards", value: "4 core" },
            { label: "Refunds (30d)", value: "< 1%" },
          ].map((stat, i) => (
            <div key={i} className="bg-white rounded-2xl border p-4 text-center">
              <div className="text-xl font-bold">{stat.value}</div>
              <div className="text-xs text-gray-500">{stat.label}</div>
            </div>
          ))}
        </div>
      </section>

      {/* Features */}
      <section id="features" className="py-12">
        <div className="max-w-6xl mx-auto px-4">
          <h2 className="text-2xl md:text-3xl font-bold text-center">Everything you need to map your millionaire path</h2>
          <div className="mt-8 grid md:grid-cols-2 lg:grid-cols-4 gap-6">
            <Feature icon={<BarChart3 className="h-5 w-5"/>} title="Portfolio Dashboard" desc="Auto-sums holdings, allocation, and total value at a glance."/>
            <Feature icon={<Coins className="h-5 w-5"/>} title="Price Target Simulator" desc="Plug future prices for XRP, XDC, ZBC, HBAR, QNT, RNDR etc. and see upside instantly."/>
            <Feature icon={<Gauge className="h-5 w-5"/>} title="Yield & Node ROI" desc="APY-based compounding with monthly contributions for DeFi and node income."/>
            <Feature icon={<Clock className="h-5 w-5"/>} title="$1M Timeline" desc="Visualizes how many months to $1,000,000 based on your inputs."/>
          </div>
          <ul className="mt-8 text-sm text-gray-600 space-y-2 max-w-3xl mx-auto">
            <li className="flex items-start gap-2"><CheckCircle2 className="h-4 w-4 mt-0.5"/> Live prices via CoinGecko formulas for Google Sheets.</li>
            <li className="flex items-start gap-2"><CheckCircle2 className="h-4 w-4 mt-0.5"/> Works with Excel offline (manual price entry) or Google Sheets online.</li>
            <li className="flex items-start gap-2"><CheckCircle2 className="h-4 w-4 mt-0.5"/> No subscriptions. Keep 100% of your data in your own drive.</li>
          </ul>
        </div>
      </section>

      {/* Live Demo Embed */}
      <section id="demo" className="py-12 bg-white border-y">
        <div className="max-w-6xl mx-auto px-4">
          <div className="flex items-baseline justify-between">
            <h3 className="text-xl md:text-2xl font-bold">Live Demo (interactive)</h3>
            <a className="text-sm underline" href={SHEET_EMBED_URL} target="_blank" rel="noreferrer">Open full screen</a>
          </div>
          <p className="text-sm text-gray-600 mt-2">This is a read‑only preview. Buyers get a private link to duplicate their own editable copy.</p>
          <div className="mt-4 rounded-2xl overflow-hidden border">
            <iframe
              src={SHEET_EMBED_URL}
              title="Crypto Millionaire Tracker – Demo"
              className="w-full h-[70vh]"
              loading="lazy"
            />
          </div>
        </div>
      </section>

      {/* Pricing */}
      <section id="pricing" className="py-14">
        <div className="max-w-6xl mx-auto px-4">
          <h3 className="text-2xl md:text-3xl font-bold text-center">Choose your plan</h3>
          <div className="mt-8 grid md:grid-cols-3 gap-6">
            <PricingCard
              name="Basic"
              price="$29"
              bullets={[
                "Manual price input",
                "Portfolio dashboard",
                "Price target simulator",
              ]}
              cta="Get Basic"
              link={GUMROAD_LINK}
            />
            <PricingCard
              featured
              name="Pro"
              price="$59"
              bullets={[
                "Live price formulas included",
                "All dashboards + charts",
                "1-click setup guide",
              ]}
              cta="Get Pro"
              link={GUMROAD_LINK}
            />
            <PricingCard
              name="Ultimate"
              price="$99"
              bullets={[
                "Yield & Node ROI sheet",
                "$1M Timeline",
                "Lifetime template updates",
              ]}
              cta="Get Ultimate"
              link={GUMROAD_LINK}
            />
          </div>
          <p className="text-center text-xs text-gray-500 mt-4">30‑day money‑back guarantee. Instant access after purchase.</p>
        </div>
      </section>

      {/* FAQ */}
      <section id="faq" className="py-12 bg-gray-50">
        <div className="max-w-5xl mx-auto px-4">
          <h3 className="text-2xl font-bold text-center">FAQ</h3>
          <div className="mt-6 grid md:grid-cols-2 gap-6">
            <FAQ q="How do live prices work?" a="In Google Sheets, we provide copy‑paste formulas that fetch USD prices from the CoinGecko API via IMPORTDATA + REGEXEXTRACT. No API key required." />
            <FAQ q="Does it work with Excel?" a="Yes. Excel version is fully functional, but live prices are manual unless you connect your own data source." />
            <FAQ q="Can I add more tokens?" a="Yes—append new rows in Portfolio and paste a matching formula in the Prices tab." />
            <FAQ q="Is this financial advice?" a="No. This template is educational and informational only." />
          </div>
        </div>
      </section>

      {/* Footer */}
      <footer className="py-10 border-t bg-white">
        <div className="max-w-6xl mx-auto px-4 flex flex-col md:flex-row items-center justify-between gap-4">
          <p className="text-sm text-gray-600">© {new Date().getFullYear()} Crypto Millionaire Tracker. All rights reserved.</p>
          <div className="flex items-center gap-4 text-sm">
            <a className="underline" href="#">Privacy</a>
            <a className="underline" href="#">Terms</a>
            <a className="underline" href={GUMROAD_LINK} target="_blank" rel="noreferrer">Get Access</a>
          </div>
        </div>
      </footer>
    </div>
  );
}

function Feature({ icon, title, desc }: { icon: React.ReactNode; title: string; desc: string }) {
  return (
    <div className="bg-white rounded-2xl p-5 border">
      <div className="h-9 w-9 rounded-xl bg-gray-100 flex items-center justify-center mb-3">{icon}</div>
      <h4 className="font-semibold">{title}</h4>
      <p className="text-sm text-gray-600 mt-1">{desc}</p>
    </div>
  );
}

function PricingCard({ name, price, bullets, cta, link, featured }: { name: string; price: string; bullets: string[]; cta: string; link: string; featured?: boolean }) {
  return (
    <div className={`rounded-2xl border p-6 bg-white ${featured ? "ring-2 ring-black" : ""}`}>
      {featured && <div className="text-xs font-semibold mb-2 inline-block px-2 py-1 rounded-full bg-black text-white">Best value</div>}
      <div className="text-lg font-semibold">{name}</div>
      <div className="text-4xl font-extrabold mt-2">{price}</div>
      <ul className="mt-4 space-y-2 text-sm text-gray-600">
        {bullets.map((b, i) => (
          <li key={i} className="flex items-start gap-2"><CheckCircle2 className="h-4 w-4 mt-0.5"/>{b}</li>
        ))}
      </ul>
      <a href={link} target="_blank" rel="noreferrer" className="mt-5 inline-flex w-full items-center justify-center gap-2 px-4 py-2 rounded-2xl bg-black text-white hover:opacity-90">
        {cta} <ArrowRight className="h-4 w-4"/>
      </a>
    </div>
  );
}

function FAQ({ q, a }: { q: string; a: string }) {
  return (
    <div className="bg-white rounded-2xl p-5 border">
      <div className="font-semibold">{q}</div>
      <p className="text-sm text-gray-600 mt-1">{a}</p>
    </div>
  );
}
