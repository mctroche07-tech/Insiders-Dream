import React, { useEffect, useMemo, useRef, useState } from "react";
import { LineChart as LineChartIcon, Newspaper, NotebookPen, Puzzle, Upload, Plus, Settings, CreditCard } from "lucide-react";
import { Card, CardContent, CardHeader, CardTitle } from "@/components/ui/card";
import { Button } from "@/components/ui/button";
import { Input } from "@/components/ui/input";
import { Textarea } from "@/components/ui/textarea";
import { Select, SelectContent, SelectItem, SelectTrigger, SelectValue } from "@/components/ui/select";
import { Tabs, TabsContent, TabsList, TabsTrigger } from "@/components/ui/tabs";
import { Label } from "@/components/ui/label";
import { Switch } from "@/components/ui/switch";
import { ResponsiveContainer, BarChart, Bar, XAxis, YAxis, Tooltip } from "recharts";

// -----------------------------------------------------------
// Trading Dashboard Starter (single-file React component)
// - Four sections (Statistics, News, Journal, Extras)
// - Top-centered nav
// - Time-anchored, customizable forms & mock data
// - LocalStorage persistence for Journal entries
// TODO: Replace mock functions with real APIs (news calendar & AI insight)
// -----------------------------------------------------------

export default function App() {
  const [active, setActive] = useState<string>("stats");

  return (
    <div className="min-h-screen bg-gradient-to-b from-slate-950 via-slate-950/95 to-slate-900 text-slate-100">
      <header className="sticky top-0 z-40 backdrop-blur border-b border-slate-800/60 bg-slate-950/70">
        <div className="mx-auto max-w-6xl px-4">
          <div className="h-16 flex items-center justify-between">
            <div className="flex items-center gap-2 font-bold tracking-tight">
              <div className="w-6 h-6 rounded-lg bg-gradient-to-br from-indigo-400 to-cyan-400 shadow"></div>
              <span>TradePilot</span>
            </div>
            <Tabs value={active} onValueChange={setActive} className="hidden md:block">
              <TabsList className="bg-slate-900/60 border border-slate-800">
                <TabsTrigger value="stats" className="gap-2"><LineChartIcon className="w-4 h-4"/>Statistics</TabsTrigger>
                <TabsTrigger value="news" className="gap-2"><Newspaper className="w-4 h-4"/>News</TabsTrigger>
                <TabsTrigger value="journal" className="gap-2"><NotebookPen className="w-4 h-4"/>Journal</TabsTrigger>
                <TabsTrigger value="extras" className="gap-2"><Puzzle className="w-4 h-4"/>Extras</TabsTrigger>
              </TabsList>
            </Tabs>
            <div className="md:hidden"/>
          </div>
        </div>
        {/* Mobile Tabs */}
        <div className="md:hidden border-t border-slate-800/60">
          <Tabs value={active} onValueChange={setActive} className="mx-auto max-w-6xl px-4">
            <TabsList className="w-full grid grid-cols-4 bg-slate-900/60 border border-slate-800 mt-2">
              <TabsTrigger value="stats" className="gap-1 text-xs">Stats</TabsTrigger>
              <TabsTrigger value="news" className="gap-1 text-xs">News</TabsTrigger>
              <TabsTrigger value="journal" className="gap-1 text-xs">Journal</TabsTrigger>
              <TabsTrigger value="extras" className="gap-1 text-xs">Extras</TabsTrigger>
            </TabsList>
          </Tabs>
        </div>
      </header>

      <main className="mx-auto max-w-6xl px-4 py-6">
        <Tabs value={active} onValueChange={setActive}>
          <TabsContent value="stats"><Statistics /></TabsContent>
          <TabsContent value="news"><News /></TabsContent>
          <TabsContent value="journal"><Journal /></TabsContent>
          <TabsContent value="extras"><Extras /></TabsContent>
        </Tabs>
      </main>
    </div>
  );
}

// ============================ Statistics =============================
function Statistics() {
  type Strategy = { id: string; name: string; params: Record<string, string | number>; };
  const defaultStrategies: Strategy[] = [
    { id: "fvg-retest", name: "FVG + Retest", params: { rr: 2, timeframe: "M15" } },
    { id: "break-retest", name: "Break & Retest", params: { rr: 1.5, timeframe: "H1" } },
    { id: "ny-open", name: "NY Open Range", params: { rr: 1.2, timeframe: "M5" } },
    { id: "ict-silver-bullet", name: "Silver Bullet (ICT)", params: { rr: 2, timeframe: "M5" } },
    { id: "ict-venom", name: "Venom (ICT)", params: { rr: 1.8, timeframe: "M15" } },
  ];

  const [strategies, setStrategies] = useState<Strategy[]>(defaultStrategies);
  const [selected, setSelected] = useState<string>(strategies[0].id);
  const [from, setFrom] = useState<string>("2024-01-01");
  const [to, setTo] = useState<string>(new Date().toISOString().slice(0,10));
  const [timeframe, setTimeframe] = useState<string>("M15");
  const [riskPerTrade, setRiskPerTrade] = useState<number>(1);
  const [trades, setTrades] = useState<number>(200);

  // Mock backtest engine — replace with real data server/API
  const result = useMemo(() => mockBacktest(selected, timeframe, from, to, trades), [selected, timeframe, from, to, trades]);

  const addStrategy = () => {
    const name = prompt("New strategy name?");
    if (!name) return;
    const id = name.toLowerCase().replace(/\s+/g, "-") + "-" + Math.random().toString(36).slice(2,6);
    setStrategies(prev => [...prev, { id, name, params: { rr: 2, timeframe: "M15" } }]);
    setSelected(id);
  };

  return (
    <div className="space-y-4">
      <div className="flex flex-wrap items-end gap-3">
        <div>
          <Label>Strategy</Label>
          <Select value={selected} onValueChange={setSelected}>
            <SelectTrigger className="w-56 bg-slate-900 border-slate-800"><SelectValue placeholder="Choose strategy" /></SelectTrigger>
            <SelectContent className="bg-slate-900 border-slate-800">
              {strategies.map(s => <SelectItem key={s.id} value={s.id}>{s.name}</SelectItem>)}
            </SelectContent>
          </Select>
        </div>
        <Button variant="secondary" onClick={addStrategy} className="gap-2"><Plus className="w-4 h-4"/>Add Strategy</Button>
        <div>
          <Label>Timeframe</Label>
          <Select value={timeframe} onValueChange={setTimeframe}>
            <SelectTrigger className="w-40 bg-slate-900 border-slate-800"><SelectValue /></SelectTrigger>
            <SelectContent className="bg-slate-900 border-slate-800">
              {["M1","M5","M15","M30","H1","H4","D1"].map(tf => <SelectItem key={tf} value={tf}>{tf}</SelectItem>)}
            </SelectContent>
          </Select>
        </div>
        <div>
          <Label>From</Label>
          <Input type="date" value={from} onChange={(e)=>setFrom(e.target.value)} className="bg-slate-900 border-slate-800" />
        </div>
        <div>
          <Label>To</Label>
          <Input type="date" value={to} onChange={(e)=>setTo(e.target.value)} className="bg-slate-900 border-slate-800" />
        </div>
        <div>
          <Label>Trades (sample)</Label>
          <Input type="number" min={20} max={2000} value={trades} onChange={(e)=>setTrades(+e.target.value)} className="bg-slate-900 border-slate-800 w-36" />
        </div>
        <div>
          <Label>Risk % / trade</Label>
          <Input type="number" min={0.1} step={0.1} value={riskPerTrade} onChange={(e)=>setRiskPerTrade(+e.target.value)} className="bg-slate-900 border-slate-800 w-36" />
        </div>
      </div>

      <div className="grid md:grid-cols-3 gap-4">
        <Card>
          <CardHeader><CardTitle>Win Rate</CardTitle></CardHeader>
          <CardContent className="text-3xl font-bold">{result.winRate}%</CardContent>
        </Card>
        <Card>
          <CardHeader><CardTitle>Expectancy</CardTitle></CardHeader>
          <CardContent className="text-3xl font-bold">{result.expectancy.toFixed(2)} R</CardContent>
        </Card>
        <Card>
          <CardHeader><CardTitle>Equity Curve (mock)</CardTitle></CardHeader>
          <CardContent className="h-40">
            <ResponsiveContainer width="100%" height="100%">
              <BarChart data={result.equity}>
                <XAxis dataKey="n" hide />
                <YAxis hide />
                <Tooltip contentStyle={{ background: "#0f172a", border: "1px solid #1f2937" }} />
                <Bar dataKey="eq" />
              </BarChart>
            </ResponsiveContainer>
          </CardContent>
        </Card>
      </div>

      <Card>
        <CardHeader><CardTitle>Notes / Scenario Builder</CardTitle></CardHeader>
        <CardContent>
          <p className="text-slate-300 text-sm">This is a starter. We’ll plug real backtesting data and your strategy rules here. You’ll be able to define entry, exit, filters (sessions, news, ADR, FVG, etc.), and save presets.</p>
        </CardContent>
      </Card>
    </div>
  );
}

function mockBacktest(strategyId: string, timeframe: string, from: string, to: string, trades: number) {
  // Deterministic-ish mock based on inputs
  const seed = (strategyId + timeframe + from + to + trades).split("").reduce((a,c)=>a + c.charCodeAt(0), 0);
  const rng = mulberry32(seed);
  const winRate = Math.round(45 + rng()*30); // 45-75%
  const expectancy = (rng()*1.4 - 0.2); // -0.2 to 1.2 R
  let eq = 0; const equity = Array.from({length: Math.min(trades, 300)}, (_,i)=>{ eq += expectancy + (rng()-0.5); return { n: i, eq: Math.max(0, eq)} });
  return { winRate, expectancy, equity };
}
function mulberry32(a:number){return function(){var t=a+=0x6D2B79F5;t=Math.imul(t^t>>>15,t|1);t^=t+Math.imul(t^t>>>7,t|61);return ((t^t>>>14)>>>0)/4294967296}}

// ============================== News ================================
function News() {
  const [date, setDate] = useState<string>(new Date().toISOString().slice(0,10));
  const [impact, setImpact] = useState<string>("all");
  const [tz, setTz] = useState<string>(Intl.DateTimeFormat().resolvedOptions().timeZone);
  const [items, setItems] = useState<any[]>(() => mockNews(date));
  const [aiOn, setAiOn] = useState<boolean>(true);

  useEffect(()=>{ setItems(mockNews(date, impact)); }, [date, impact]);

  return (
    <div className="space-y-4">
      <div className="flex flex-wrap items-end gap-3">
        <div>
          <Label>Date</Label>
          <Input type="date" className="bg-slate-900 border-slate-800" value={date} onChange={e=>setDate(e.target.value)} />
        </div>
        <div>
          <Label>Impact</Label>
          <Select value={impact} onValueChange={setImpact}>
            <SelectTrigger className="w-40 bg-slate-900 border-slate-800"><SelectValue /></SelectTrigger>
            <SelectContent className="bg-slate-900 border-slate-800">
              <SelectItem value="all">All</SelectItem>
              <SelectItem value="low">Low</SelectItem>
              <SelectItem value="medium">Medium</SelectItem>
              <SelectItem value="high">High</SelectItem>
            </SelectContent>
          </Select>
        </div>
        <div>
          <Label>Timezone</Label>
          <Input value={tz} onChange={e=>setTz(e.target.value)} className="bg-slate-900 border-slate-800 w-60" />
        </div>
        <Button onClick={()=>setItems(mockNews(date, impact))}>Refresh (mock)</Button>
      </div>

      <Card>
        <CardHeader><CardTitle>Economic Calendar (sample data)</CardTitle></CardHeader>
        <CardContent className="overflow-auto">
          <table className="w-full text-sm">
            <thead className="text-slate-300">
              <tr className="border-b border-slate-800">
                <th className="text-left py-2">Time</th>
                <th className="text-left">Currency</th>
                <th className="text-left">Event</th>
                <th className="text-left">Impact</th>
                <th className="text-right">Forecast</th>
                <th className="text-right">Previous</th>
                <th className="text-right">Actual</th>
              </tr>
            </thead>
            <tbody>
              {items.map((it, i)=> (
                <tr key={i} className="border-b border-slate-900/60 hover:bg-slate-900/40">
                  <td className="py-2">{it.time}</td>
                  <td>{it.ccy}</td>
                  <td>{it.title}</td>
                  <td className="capitalize">{it.impact}</td>
                  <td className="text-right">{it.forecast ?? "—"}</td>
                  <td className="text-right">{it.previous ?? "—"}</td>
                  <td className="text-right">{it.actual ?? "—"}</td>
                </tr>
              ))}
            </tbody>
          </table>
        </CardContent>
      </Card>

      <Card>
        <CardHeader><CardTitle>AI Insight (prototype)</CardTitle></CardHeader>
        <CardContent>
          <div className="flex items-center gap-3 mb-3">
            <Switch checked={aiOn} onCheckedChange={setAiOn} />
            <span className="text-sm text-slate-300">Enable AI commentary</span>
          </div>
          <p className="text-slate-300 text-sm">{aiOn ? aiInsight(items) : "(AI off)"}</p>
          <p className="text-slate-400 text-xs mt-2">TODO: wire to a news API + AI endpoint to analyze event surprises by currency & session.</p>
        </CardContent>
      </Card>
    </div>
  );
}

function mockNews(date: string, impact: string = "all") {
  const base = [
    { time: "08:30", ccy: "USD", title: "Non-Farm Payrolls", impact: "high", forecast: "+170k", previous: "+187k", actual: "—" },
    { time: "07:00", ccy: "GBP", title: "BoE Gov Speech", impact: "medium", forecast: null, previous: null, actual: null },
    { time: "10:00", ccy: "EUR", title: "CPI (YoY)", impact: "high", forecast: "2.8%", previous: "3.1%", actual: "—" },
    { time: "13:30", ccy: "CAD", title: "Unemployment Rate", impact: "medium", forecast: "5.7%", previous: "5.6%", actual: "—" },
    { time: "23:50", ccy: "JPY", title: "GDP (QoQ)", impact: "low", forecast: "0.2%", previous: "0.1%", actual: "—" },
  ];
  const f = impact === "all" ? base : base.filter(b => b.impact === impact);
  return f;
}
function aiInsight(items: any[]) {
  const high = items.filter(i=>i.impact === "high");
  if (high.length) {
    const ccySet = Array.from(new Set(high.map(h=>h.ccy))).join(", ");
    return `High-impact (${ccySet}) today. Expect wider ranges around release times; consider smaller size pre-event and fade/continuation setups on the first pullback after actuals.`;
  }
  return "Calendar is light-to-medium impact. Mean-reversion setups in Asia/London, watch overlap for liquidity spikes.";
}

// ============================== Journal =============================
function Journal() {
  type Entry = { id: string; date: string; pnl: number; rr: number; reason: string; image?: string };
  const [entries, setEntries] = useState<Entry[]>(()=>{
    const raw = localStorage.getItem("journal.entries");
    return raw ? JSON.parse(raw) as Entry[] : [];
  });
  useEffect(()=>{ localStorage.setItem("journal.entries", JSON.stringify(entries)); }, [entries]);

  const [date, setDate] = useState<string>(new Date().toISOString().slice(0,10));
  const [pnl, setPnl] = useState<number>(0);
  const [rr, setRR] = useState<number>(1.0);
  const [reason, setReason] = useState<string>("");
  const [image, setImage] = useState<string|undefined>(undefined);

  const fileRef = useRef<HTMLInputElement>(null);
  const onImage = (e: React.ChangeEvent<HTMLInputElement>) => {
    const f = e.target.files?.[0];
    if (!f) return;
    const url = URL.createObjectURL(f);
    setImage(url);
  };

  const addEntry = () => {
    const id = crypto.randomUUID();
    const entry: Entry = { id, date, pnl: Number(pnl), rr: Number(rr), reason, image };
    setEntries([entry, ...entries]);
    setReason("");
    setPnl(0);
    setRR(1.0);
    setImage(undefined);
    if (fileRef.current) fileRef.current.value = "";
  };

  const stats = useMemo(()=> summarize(entries), [entries]);

  return (
    <div className="space-y-4">
      <Card>
        <CardHeader><CardTitle>New Journal Entry</CardTitle></CardHeader>
        <CardContent className="grid md:grid-cols-2 gap-4">
          <div className="space-y-3">
            <div>
              <Label>Date</Label>
              <Input type="date" value={date} onChange={e=>setDate(e.target.value)} className="bg-slate-900 border-slate-800" />
            </div>
            <div className="grid grid-cols-2 gap-3">
              <div>
                <Label>P/L</Label>
                <Input type="number" value={pnl} onChange={e=>setPnl(+e.target.value)} className="bg-slate-900 border-slate-800" placeholder="e.g., 150" />
              </div>
              <div>
                <Label>Risk : Reward</Label>
                <Input type="number" step="0.1" value={rr} onChange={e=>setRR(+e.target.value)} className="bg-slate-900 border-slate-800" placeholder="e.g., 2.0" />
              </div>
            </div>
            <div>
              <Label>Reason / Notes</Label>
              <Textarea value={reason} onChange={e=>setReason(e.target.value)} className="bg-slate-900 border-slate-800" rows={5} />
            </div>
          </div>
          <div className="space-y-3">
            <Label>Screenshot</Label>
            <Input ref={fileRef} type="file" accept="image/*" onChange={onImage} className="bg-slate-900 border-slate-800" />
            {image && <img src={image} alt="Trade screenshot" className="rounded-lg border border-slate-800" />}
            <Button onClick={addEntry} className="mt-2">Save Entry</Button>
            <Card className="mt-3">
              <CardHeader><CardTitle>AI Insight (prototype)</CardTitle></CardHeader>
              <CardContent>
                <p className="text-sm text-slate-300">{aiInsightFromEntry({ pnl, rr, reason })}</p>
                <p className="text-xs text-slate-400 mt-2">TODO: connect to AI backend for tailored feedback per entry and across history.</p>
              </CardContent>
            </Card>
          </div>
        </CardContent>
      </Card>

      <div className="grid lg:grid-cols-3 gap-4">
        <Card className="lg:col-span-1">
          <CardHeader><CardTitle>Performance Overview</CardTitle></CardHeader>
          <CardContent>
            <ul className="text-sm space-y-1 text-slate-300">
              <li>Total Entries: {stats.count}</li>
              <li>Win Rate: {stats.winRate}%</li>
              <li>Average P/L: {stats.avgPnl.toFixed(2)}</li>
              <li>Best Day: {stats.bestDay?.date ?? "—"} ({stats.bestDay ? stats.bestDay.pnl : "—"})</li>
            </ul>
            <div className="h-32 mt-3">
              <ResponsiveContainer width="100%" height="100%">
                <BarChart data={stats.byDay}>
                  <XAxis dataKey="date" hide />
                  <YAxis hide />
                  <Tooltip contentStyle={{ background: "#0f172a", border: "1px solid #1f2937" }} />
                  <Bar dataKey="pnl" />
                </BarChart>
              </ResponsiveContainer>
            </div>
          </CardContent>
        </Card>
        <Card className="lg:col-span-2">
          <CardHeader><CardTitle>Journal Entries</CardTitle></CardHeader>
          <CardContent className="space-y-3">
            {entries.length === 0 && <p className="text-slate-400 text-sm">No entries yet.</p>}
            {entries.map(e => (
              <div key={e.id} className="border border-slate-800 rounded-xl p-3 grid md:grid-cols-6 gap-3 bg-slate-900/60">
                <div className="md:col-span-2">
                  {e.image ? <img src={e.image} className="rounded-lg border border-slate-800" /> : <div className="h-24 rounded-lg bg-slate-800/40 flex items-center justify-center text-slate-400">No image</div>}
                </div>
                <div className="md:col-span-4 grid sm:grid-cols-2 gap-3">
                  <div>
                    <div className="text-xs text-slate-400">Date</div>
                    <div>{e.date}</div>
                  </div>
                  <div>
                    <div className="text-xs text-slate-400">P/L</div>
                    <div className={e.pnl>=0 ? "text-emerald-400" : "text-rose-400"}>{e.pnl}</div>
                  </div>
                  <div>
                    <div className="text-xs text-slate-400">R:R</div>
                    <div>{e.rr}</div>
                  </div>
                  <div className="sm:col-span-2">
                    <div className="text-xs text-slate-400">Reason</div>
                    <div className="line-clamp-3">{e.reason}</div>
                  </div>
                </div>
              </div>
            ))}
          </CardContent>
        </Card>
      </div>
    </div>
  );
}

function summarize(entries: {date:string,pnl:number}[]) {
  const count = entries.length;
  const wins = entries.filter(e=>e.pnl>0).length;
  const winRate = count ? Math.round(100*wins/count) : 0;
  const avgPnl = count ? entries.reduce((a,b)=>a+b.pnl,0)/count : 0;
  const map = new Map<string, number>();
  entries.forEach(e=>{ map.set(e.date, (map.get(e.date)||0)+e.pnl); });
  const byDay = Array.from(map.entries()).map(([date,pnl])=>({ date, pnl }));
  const bestDay = byDay.sort((a,b)=>b.pnl-a.pnl)[0];
  return { count, winRate, avgPnl, byDay, bestDay };
}

function aiInsightFromEntry(e: { pnl:number, rr:number, reason:string }) {
  let tips = [] as string[];
  if (e.rr < 1) tips.push("Consider improving R:R or using partials to lift expectancy.");
  if (e.pnl < 0) tips.push("Loss day — review entry timing and stop placement; check if news/sessions conflicted.");
  if ((e.reason||"").length < 15) tips.push("Add more detail to your reason; it helps pattern recognition later.");
  if (!tips.length) tips.push("Solid trade. Keep journaling detail and review sequences, not single outcomes.");
  return tips.join(" ");
}

// ============================== Extras ===============================
function Extras() {
  return (
    <div className="space-y-4">
      <div className="grid md:grid-cols-3 gap-4">
        <Card>
          <CardHeader><CardTitle className="flex items-center gap-2"><Puzzle className="w-4 h-4"/>Indicators</CardTitle></CardHeader>
          <CardContent className="space-y-3">
            <p className="text-sm text-slate-300">List your TradingView indicators here. Paste links or IDs.</p>
            <Input placeholder="tv/indicator-link-or-id" className="bg-slate-900 border-slate-800" />
            <Button variant="secondary">Add</Button>
            <div className="text-xs text-slate-400">TODO: embed previews or screenshots.</div>
          </CardContent>
        </Card>
        <Card>
          <CardHeader><CardTitle className="flex items-center gap-2"><Settings className="w-4 h-4"/>Settings</CardTitle></CardHeader>
          <CardContent className="space-y-3">
            <Label>Default Timezone</Label>
            <Input defaultValue={Intl.DateTimeFormat().resolvedOptions().timeZone} className="bg-slate-900 border-slate-800" />
            <Label>Theme</Label>
            <Select defaultValue="system">
              <SelectTrigger className="bg-slate-900 border-slate-800 w-40"><SelectValue /></SelectTrigger>
              <SelectContent className="bg-slate-900 border-slate-800">
                <SelectItem value="system">System</SelectItem>
                <SelectItem value="dark">Dark</SelectItem>
                <SelectItem value="light">Light</SelectItem>
              </SelectContent>
            </Select>
          </CardContent>
        </Card>
        <Card>
          <CardHeader><CardTitle className="flex items-center gap-2"><CreditCard className="w-4 h-4"/>Subscription</CardTitle></CardHeader>
          <CardContent className="space-y-3">
            <p className="text-sm text-slate-300">Manage your billing plan.</p>
            <div className="grid grid-cols-2 gap-2">
              <Button variant="secondary">Change Plan</Button>
              <Button>Manage Billing</Button>
            </div>
            <p className="text-xs text-slate-400">TODO: connect to Stripe customer portal.</p>
          </CardContent>
        </Card>
      </div>
    </div>
  );
}
