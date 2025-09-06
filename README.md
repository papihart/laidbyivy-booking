const CONFIG = {
  brand: {
    nameLarge: "YVAELLA",
    domain: "Laidbyivy.co",
    artistFirstName: "Ivy",
    tagline: "Welcome to my page",
    about:
      "Hi, my name is Ivy, I’m 21 years old and a passionate hairstylist specializing in wig installations and sew‑ins. My goal is to help every client feel confident and beautiful with a flawless, natural look. With creativity, precision, and care, I make sure each style is customized just for you.",
    hours: "9AM to 11PM",
    days: "LUN • MAR • MER • JEU • VEN • SAM • DIM",
    location: "3565 Rue Jarry Est (Suite 110), Montréal",
    phone: "438‑354‑7520",
    instagram: "@laidbyivy_co",
    email: "yvaellacedar@gmail.com",
  },
  theme: {
    // colors
    bg: "#0f0f12",
    panel: "#1a1614",
    card: "#2a2320",
    gold: "#f0c693",
    goldBright: "#ffd7a0",
    copper: "#cb9065",
    ring: "#8e6a51",
  },
};

const Container = ({ children, className = "" }) => (
  <div className={`mx-auto max-w-[1100px] px-4 ${className}`}>{children}</div>
);

const Glow = ({ children, className = "", glow = "0 0 24px rgba(255,215,160,.35)" }) => (
  <span style={{ textShadow: glow }} className={className}>{children}</span>
);

const Pill = ({ children }) => (
  <span className="inline-flex items-center rounded-full bg-[rgba(255,215,160,0.08)] border border-[rgba(255,215,160,0.25)] px-3 py-1 text-[12px] tracking-wide">
    {children}
  </span>
);

const Divider = () => (
  <div className="h-px w-full bg-gradient-to-r from-transparent via-[rgba(255,215,160,0.35)] to-transparent"/>
);

const Panel = ({ children, className = "" }) => (
  <div className={`rounded-[18px] border border-[rgba(255,215,160,0.25)] bg-[rgba(255,215,160,0.04)] ${className}`}>{children}</div>
);

const SectionTitle = ({ pre, main }) => (
  <div className="text-center">
    {pre && (
      <p className="text-[13px] uppercase tracking-[0.35em] text-[rgba(255,215,160,0.8)] mb-1">{pre}</p>
    )}
    <h2 className="text-[36px] md:text-[44px] font-serif text-white">
      <Glow>{main}</Glow>
    </h2>
  </div>
);

const Hero = () => (
  <section className="relative border-y border-[rgba(255,215,160,0.25)]" style={{ background: `radial-gradient(1200px 600px at 50% -10%, rgba(255,215,160,0.08), transparent), linear-gradient(180deg, rgba(0,0,0,.4), rgba(0,0,0,.4))` }}>
    <div className="absolute inset-0 -z-10">
      <img src="/images/hero.jpg" alt="Hero background" className="h-full w-full object-cover opacity-45" />
    </div>
    <Container className="py-12 md:py-16">
      <p className="text-[12px] uppercase tracking-[0.4em] text-[rgba(255,215,160,0.8)] text-center">{CONFIG.brand.tagline}</p>
      <h1 className="mt-1 text-center text-[52px] md:text-[96px] leading-none font-serif text-white">
        {CONFIG.brand.nameLarge}
      </h1>
      <p className="mt-1 text-center text-[28px] md:text-[40px] text-white/90 font-serif">
        <Glow className="italic">{CONFIG.brand.domain}</Glow>
      </p>

      <div className="mt-10 grid md:grid-cols-[1fr,340px] gap-10 items-center">
        <div>
          <h3 className="text-[38px] md:text-[48px] text-white/90 font-serif tracking-wide">
            MEET YOUR <Glow className="italic" glow="0 0 18px rgba(255,215,160,.45)">artist</Glow>
          </h3>
          <p className="mt-4 text-[14px] leading-relaxed text-[rgba(255,255,255,0.82)] max-w-2xl">
            {CONFIG.brand.about}
          </p>
        </div>
        <div className="flex justify-center md:justify-end">
          <div className="relative">
            <div className="absolute inset-0 rounded-full blur-xl" style={{ boxShadow: "0 0 60px rgba(255,215,160,.35)" }} />
            <img src="/images/artist.jpg" alt="Artist" className="relative h-[220px] w-[220px] object-cover rounded-full ring-2" style={{ ringColor: CONFIG.theme.ring }} />
          </div>
        </div>
      </div>

      <div className="mt-10 grid md:grid-cols-2 gap-6">
        <Panel className="p-6">
          <p className="text-[22px] text-white font-serif">OUR <Glow className="italic">Hours</Glow></p>
          <Divider/>
          <p className="mt-4 text-[28px] md:text-[34px] text-white font-semibold">{CONFIG.brand.hours}</p>
          <Pill className="mt-3"/>
          <div className="mt-3 text-[12px] tracking-[.25em] text-white/80">{CONFIG.brand.days}</div>
        </Panel>
        <Panel className="p-6">
          <p className="text-[22px] text-white font-serif">LOCATION</p>
          <Divider/>
          <p className="mt-4 text-[18px] md:text-[22px] text-white font-semibold leading-snug">{CONFIG.brand.location}</p>
          <div className="mt-3 text-[12px] tracking-[.25em] text-white/70 uppercase">(Montreal)</div>
        </Panel>
      </div>
    </Container>
  </section>
);

const PolicyCard = ({ title, text, icon }) => (
  <Panel className="p-5">
    <div className="flex items-center gap-3">
      <div className="h-9 w-9 rounded-md bg-[rgba(255,215,160,0.12)] flex items-center justify-center text-[rgba(255,215,160,0.85)]">{icon || "★"}</div>
      <h4 className="text-[16px] text-white font-semibold">{title}</h4>
    </div>
    <p className="mt-2 text-[13px] leading-relaxed text-white/85">{text}</p>
  </Panel>
);

const Policies = () => (
  <section className="py-14">
    <Container>
      <SectionTitle pre="our" main={<><Glow className="italic">Policies</Glow></>} />
      <div className="mt-8 grid md:grid-cols-3 gap-6">
        <PolicyCard title="HAIR DROP‑OFF" text="Drop‑off for customization should be made at least 48h before your appointment." />
        <PolicyCard title="CANCELLATIONS" text="You must cancel or reschedule at least 48 hours before your appointment." />
        <PolicyCard title="BOOKING POLICY" text="All appointments must be booked at least 72 hours in advance." />
      </div>
      <div className="mt-6 grid md:grid-cols-3 gap-6">
        <PolicyCard title="DEPOSITS" text="A $20 non‑refundable deposit is required to secure your spot." />
        <PolicyCard title="SQUEEZE IN" text="$30 squeeze‑in fee may apply for same‑day/after‑hours requests." />
        <PolicyCard title="LATE ARRIVALS" text="After 15 minutes, a late fee applies. Over 20 minutes may result in cancellation." />
      </div>
      <div className="mt-6 grid md:grid-cols-3 gap-6">
        <PolicyCard title="RESCHEDULE" text="One time reschedule is allowed if proper notice is given." />
        <div className="md:col-span-2 flex items-center">
          <h3 className="text-[38px] md:text-[48px] text-white/90 font-serif tracking-wide">
            BOOKING <Glow className="italic">Rules</Glow>
          </h3>
        </div>
      </div>
    </Container>
  </section>
);

const ThankYou = () => (
  <section className="py-16">
    <Container>
      <Panel className="p-8">
        <div className="grid md:grid-cols-[220px,1fr,220px] gap-6 items-center">
          <div className="hidden md:block">
            <div className="rounded-[26px] overflow-hidden border border-[rgba(255,215,160,0.25)]">
              <img src="/images/phone1.jpg" alt="Style 1" className="h-[360px] w-full object-cover"/>
            </div>
          </div>
          <div className="text-center">
            <p className="text-[36px] md:text-[44px] text-white font-serif"><Glow>THANK YOU</Glow></p>
            <p className="text-[18px] text-white/85 italic">for choosing us</p>
            <p className="mt-2 text-[12px] text-white/70">Please choose the services below</p>
            <div className="mt-6 flex justify-center">
              <a href="#booking" className="group inline-flex items-center gap-3 rounded-full border border-[rgba(255,215,160,0.5)] px-6 py-3">
                <span className="grid place-items-center h-9 w-9 rounded-full border border-[rgba(255,215,160,0.5)]">→</span>
                <span className="text-[16px] font-semibold text-white"><Glow>BOOK NOW</Glow></span>
              </a>
            </div>
          </div>
          <div className="hidden md:block">
            <div className="rounded-[26px] overflow-hidden border border-[rgba(255,215,160,0.25)]">
              <img src="/images/phone2.jpg" alt="Style 2" className="h-[360px] w-full object-cover"/>
            </div>
          </div>
        </div>
      </Panel>
      <p className="mt-10 text-center text-[28px] md:text-[36px] text-white font-serif"><Glow>thank you for booking</Glow></p>
    </Container>
  </section>
);

const Footer = () => (
  <footer className="border-t border-[rgba(255,215,160,0.25)]">
    <Container className="py-6">
      <div className="flex flex-col md:flex-row items-center justify-between gap-4 text-[13px] text-white/85">
        <div className="flex items-center gap-2">
          <span>📞</span>
          <span>{CONFIG.brand.phone}</span>
        </div>
        <div className="flex items-center gap-2">
          <span>📷</span>
          <span>{CONFIG.brand.instagram}</span>
        </div>
        <div className="flex items-center gap-2">
          <span>✉️</span>
          <span>{CONFIG.brand.email}</span>
        </div>
      </div>
    </Container>
  </footer>
);

export default function YvaellaLookMock() {
  React.useEffect(() => {
    document.body.style.background = CONFIG.theme.bg;
  }, []);
  return (
    <div className="text-[15px]" style={{ color: CONFIG.theme.goldBright }}>
      <div className="text-white">
        <Hero/>
        <Policies/>
        <ThankYou/>
        <Footer/>
      </div>
    </div>
  );
}
