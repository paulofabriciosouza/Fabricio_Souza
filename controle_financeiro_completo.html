<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="utf-8" />
<meta name="viewport" content="width=device-width,initial-scale=1" />
<title>Controle Financeiro — Completo</title>
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<style>
  :root{
    --bg:#f4f7fa; --card:#fff; --accent:#3498db; --accent-2:#2ecc71;
    --muted:#95a5a6; --text:#2c3e50;
    --danger:#e74c3c;
  }
  [data-theme="dark"]{
    --bg:#121416; --card:#1b1d20; --accent:#0abf9c; --accent-2:#2ecc71;
    --muted:#3b4350; --text:#e6eef3;
    --danger:#ff6b6b;
  }
  *{box-sizing:border-box}
  body{
    margin:0; padding:20px; font-family:Inter, "Segoe UI", Arial, sans-serif;
    background:var(--bg); color:var(--text);
  }
  h1{text-align:center; margin:4px 0 18px; font-weight:700}
  .wrap{max-width:1200px; margin:0 auto}
  .top-controls{display:flex; gap:8px; flex-wrap:wrap; justify-content:center; margin-bottom:12px}
  .top-controls button, .top-controls input[type="file"]{
    padding:8px 12px; border-radius:8px; border:none; cursor:pointer; font-weight:600;
    background:var(--muted); color:#fff;
  }
  .theme-switch{background:var(--accent); border:none; color:#fff;}
  #tabs{display:flex; flex-wrap:wrap; gap:8px; justify-content:center; margin-bottom:18px}
  #tabs button{
    padding:8px 14px; border-radius:8px; border:none; cursor:pointer; font-weight:600;
    background:var(--muted); color:#fff;
  }
  #tabs button.active{background:var(--accent-2)}
  .month-content{
    display:none; background:var(--card); padding:18px; border-radius:10px;
    box-shadow:0 6px 18px rgba(14,30,37,0.06); margin-bottom:24px;
  }
  .month-content.active{display:block}
  .earnings-row{display:flex; gap:12px; flex-wrap:wrap; align-items:flex-start}
  .earn-block{flex:1 1 260px; background:#fbfdff; padding:12px; border-radius:8px; border:1px solid rgba(0,0,0,0.04)}
  [data-theme="dark"] .earn-block{background:#141617}
  .earn-block label{font-size:13px; color:#333; display:block; margin-bottom:6px}
  .earn-block input{width:100%; padding:8px; border-radius:6px; border:1px solid #d6e6f2}
  .totals{display:flex; gap:12px; flex-wrap:wrap; margin-top:10px}
  .totals p{margin:6px 0; padding:10px 12px; background:linear-gradient(180deg,#fff,#f7fbff); border-radius:8px; border:1px solid rgba(0,0,0,0.03)}
  [data-theme="dark"] .totals p{background:transparent; border:1px solid rgba(255,255,255,0.04)}
  table{width:100%; border-collapse:collapse; margin-top:10px}
  th,td{padding:10px; border:1px solid #eef4fa; vertical-align:middle; text-align:left; font-size:14px}
  thead th{background:var(--accent); color:#fff}
  tbody tr:nth-child(even){background:#fbfdff}
  [data-theme="dark"] thead th{background:transparent; color:var(--text); border-bottom:1px solid rgba(255,255,255,0.06)}
  [data-theme="dark"] tbody tr:nth-child(even){background:transparent}
  .actions button{background:var(--danger); border:none; color:#fff; padding:6px 8px; border-radius:6px; cursor:pointer}
  .add-btn{margin-top:8px; background:var(--accent); color:#fff; border:none; padding:8px 12px; border-radius:8px; cursor:pointer}
  .charts-row{display:flex; gap:16px; flex-wrap:wrap; margin-top:14px; align-items:flex-start}
  .chart-wrap{flex:1 1 360px; background:#fff; border-radius:8px; padding:10px; box-shadow:0 4px 12px rgba(0,0,0,0.04); text-align:center}
  [data-theme="dark"] .chart-wrap{background:transparent; box-shadow:none}
  canvas{max-width:100%; height:300px}
  @media(max-width:880px){
    .earnings-row{flex-direction:column}
    .chart-wrap{flex:1 1 100%}
  }
  .small{font-size:13px; color:#444}
  .inline-grid{display:grid; grid-template-columns:1fr 1fr; gap:10px; align-items:start}
  .desc-input{width:100%; padding:8px; border-radius:6px; border:1px solid #d6e6f2}
  .month-actions{display:flex; gap:8px; justify-content:flex-end; margin-bottom:8px}
  .danger{background:var(--danger); color:#fff; border:none; padding:6px 8px; border-radius:6px; cursor:pointer}
  .muted{background:var(--muted); color:#fff; border:none; padding:6px 8px; border-radius:6px; cursor:pointer}
  .file-input{display:none}
</style>
</head>
<body>
<div class="wrap" id="app">
  <h1>Controle Financeiro — Completo</h1>

  <div class="top-controls">
    <button class="theme-switch" onclick="toggleTheme()">Alternar Tema</button>
    <button onclick="exportAll()">Exportar (JSON)</button>
    <label style="display:inline-block;">
      <input id="importFile" class="file-input" type="file" accept="application/json" onchange="importFile(event)">
      <button class="muted" onclick="document.getElementById('importFile').click()">Importar (JSON)</button>
    </label>
    <button onclick="clearAllData()" class="muted">Limpar TODOS os dados</button>
  </div>

  <div id="tabs">
    <button data-month="jan" onclick="showMonth('jan')">Janeiro</button>
    <button data-month="fev" onclick="showMonth('fev')">Fevereiro</button>
    <button data-month="mar" onclick="showMonth('mar')">Março</button>
    <button data-month="abr" onclick="showMonth('abr')">Abril</button>
    <button data-month="mai" onclick="showMonth('mai')">Maio</button>
    <button data-month="jun" onclick="showMonth('jun')">Junho</button>
    <button data-month="jul" onclick="showMonth('jul')">Julho</button>
    <button data-month="ago" onclick="showMonth('ago')">Agosto</button>
    <button data-month="set" onclick="showMonth('set')">Setembro</button>
    <button data-month="out" onclick="showMonth('out')">Outubro</button>
    <button data-month="nov" onclick="showMonth('nov')">Novembro</button>
    <button data-month="dez" onclick="showMonth('dez')">Dezembro</button>
  </div>

  <!-- Months blocks (abbreviated repetition of previous full blocks) -->
  <!-- For brevity and reliability, include all months similarly to earlier code -->

  <div id="content_jan" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Janeiro</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('jan')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_jan" step="0.01" oninput="calc('jan'); saveData('jan')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_jan" step="0.01" oninput="calc('jan'); saveData('jan')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_jan">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_jan" step="0.01" oninput="calc('jan'); saveData('jan')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_jan" step="0.01" oninput="calc('jan'); saveData('jan')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_jan">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_jan" step="0.01" oninput="calc('jan'); saveData('jan')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_jan" step="0.01" oninput="calc('jan'); saveData('jan')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_jan">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_jan">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_jan">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_jan">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_jan">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_jan">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_jan">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','jan')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_jan">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','jan')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_jan"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_jan"></canvas>
      </div>
    </div>
  </div>

  <div id="content_fev" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Fevereiro</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('fev')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_fev" step="0.01" oninput="calc('fev'); saveData('fev')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_fev" step="0.01" oninput="calc('fev'); saveData('fev')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_fev">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_fev" step="0.01" oninput="calc('fev'); saveData('fev')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_fev" step="0.01" oninput="calc('fev'); saveData('fev')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_fev">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_fev" step="0.01" oninput="calc('fev'); saveData('fev')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_fev" step="0.01" oninput="calc('fev'); saveData('fev')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_fev">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_fev">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_fev">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_fev">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_fev">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_fev">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_fev">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','fev')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_fev">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','fev')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_fev"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_fev"></canvas>
      </div>
    </div>
  </div>

  <div id="content_mar" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Março</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('mar')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_mar" step="0.01" oninput="calc('mar'); saveData('mar')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_mar" step="0.01" oninput="calc('mar'); saveData('mar')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_mar">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_mar" step="0.01" oninput="calc('mar'); saveData('mar')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_mar" step="0.01" oninput="calc('mar'); saveData('mar')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_mar">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_mar" step="0.01" oninput="calc('mar'); saveData('mar')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_mar" step="0.01" oninput="calc('mar'); saveData('mar')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_mar">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_mar">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_mar">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_mar">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_mar">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_mar">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_mar">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','mar')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_mar">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','mar')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_mar"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_mar"></canvas>
      </div>
    </div>
  </div>

  <div id="content_abr" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Abril</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('abr')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_abr" step="0.01" oninput="calc('abr'); saveData('abr')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_abr" step="0.01" oninput="calc('abr'); saveData('abr')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_abr">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_abr" step="0.01" oninput="calc('abr'); saveData('abr')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_abr" step="0.01" oninput="calc('abr'); saveData('abr')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_abr">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_abr" step="0.01" oninput="calc('abr'); saveData('abr')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_abr" step="0.01" oninput="calc('abr'); saveData('abr')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_abr">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_abr">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_abr">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_abr">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_abr">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_abr">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_abr">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','abr')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_abr">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','abr')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_abr"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_abr"></canvas>
      </div>
    </div>
  </div>

  <div id="content_mai" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Maio</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('mai')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_mai" step="0.01" oninput="calc('mai'); saveData('mai')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_mai" step="0.01" oninput="calc('mai'); saveData('mai')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_mai">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_mai" step="0.01" oninput="calc('mai'); saveData('mai')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_mai" step="0.01" oninput="calc('mai'); saveData('mai')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_mai">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_mai" step="0.01" oninput="calc('mai'); saveData('mai')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_mai" step="0.01" oninput="calc('mai'); saveData('mai')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_mai">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_mai">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_mai">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_mai">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_mai">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_mai">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_mai">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','mai')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_mai">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','mai')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_mai"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_mai"></canvas>
      </div>
    </div>
  </div>

  <div id="content_jun" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Junho</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('jun')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_jun" step="0.01" oninput="calc('jun'); saveData('jun')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_jun" step="0.01" oninput="calc('jun'); saveData('jun')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_jun">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_jun" step="0.01" oninput="calc('jun'); saveData('jun')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_jun" step="0.01" oninput="calc('jun'); saveData('jun')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_jun">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_jun" step="0.01" oninput="calc('jun'); saveData('jun')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_jun" step="0.01" oninput="calc('jun'); saveData('jun')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_jun">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_jun">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_jun">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_jun">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_jun">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_jun">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_jun">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','jun')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_jun">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','jun')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_jun"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_jun"></canvas>
      </div>
    </div>
  </div>

  <div id="content_jul" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Julho</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('jul')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_jul" step="0.01" oninput="calc('jul'); saveData('jul')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_jul" step="0.01" oninput="calc('jul'); saveData('jul')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_jul">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_jul" step="0.01" oninput="calc('jul'); saveData('jul')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_jul" step="0.01" oninput="calc('jul'); saveData('jul')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_jul">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_jul" step="0.01" oninput="calc('jul'); saveData('jul')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_jul" step="0.01" oninput="calc('jul'); saveData('jul')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_jul">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_jul">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_jul">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_jul">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_jul">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_jul">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_jul">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','jul')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_jul">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','jul')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_jul"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_jul"></canvas>
      </div>
    </div>
  </div>

  <div id="content_ago" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Agosto</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('ago')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_ago" step="0.01" oninput="calc('ago'); saveData('ago')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_ago" step="0.01" oninput="calc('ago'); saveData('ago')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_ago">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_ago" step="0.01" oninput="calc('ago'); saveData('ago')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_ago" step="0.01" oninput="calc('ago'); saveData('ago')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_ago">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_ago" step="0.01" oninput="calc('ago'); saveData('ago')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_ago" step="0.01" oninput="calc('ago'); saveData('ago')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_ago">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_ago">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_ago">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_ago">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_ago">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_ago">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_ago">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','ago')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_ago">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','ago')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_ago"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_ago"></canvas>
      </div>
    </div>
  </div>

  <div id="content_set" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Setembro</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('set')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_set" step="0.01" oninput="calc('set'); saveData('set')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_set" step="0.01" oninput="calc('set'); saveData('set')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_set">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_set" step="0.01" oninput="calc('set'); saveData('set')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_set" step="0.01" oninput="calc('set'); saveData('set')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_set">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_set" step="0.01" oninput="calc('set'); saveData('set')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_set" step="0.01" oninput="calc('set'); saveData('set')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_set">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_set">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_set">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_set">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_set">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_set">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_set">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','set')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_set">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','set')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_set"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_set"></canvas>
      </div>
    </div>
  </div>

  <div id="content_out" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Outubro</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('out')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_out" step="0.01" oninput="calc('out'); saveData('out')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_out" step="0.01" oninput="calc('out'); saveData('out')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_out">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_out" step="0.01" oninput="calc('out'); saveData('out')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_out" step="0.01" oninput="calc('out'); saveData('out')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_out">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_out" step="0.01" oninput="calc('out'); saveData('out')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_out" step="0.01" oninput="calc('out'); saveData('out')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_out">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_out">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_out">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_out">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_out">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_out">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_out">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','out')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_out">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','out')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_out"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_out"></canvas>
      </div>
    </div>
  </div>

  <div id="content_nov" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Novembro</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('nov')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_nov" step="0.01" oninput="calc('nov'); saveData('nov')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_nov" step="0.01" oninput="calc('nov'); saveData('nov')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_nov">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_nov" step="0.01" oninput="calc('nov'); saveData('nov')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_nov" step="0.01" oninput="calc('nov'); saveData('nov')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_nov">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_nov" step="0.01" oninput="calc('nov'); saveData('nov')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_nov" step="0.01" oninput="calc('nov'); saveData('nov')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_nov">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_nov">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_nov">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_nov">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_nov">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_nov">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_nov">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','nov')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_nov">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','nov')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_nov"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_nov"></canvas>
      </div>
    </div>
  </div>

  <div id="content_dez" class="month-content">
    <div class="month-actions">
      <div style="flex:1"><h2 style="margin:0">Dezembro</h2></div>
      <div>
        <button class="muted" onclick="clearMonth('dez')">🧹 Limpar Mês</button>
      </div>
    </div>

    <div class="earnings-row">
      <div class="earn-block">
        <strong>Dia 15</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d15_michely_dez" step="0.01" oninput="calc('dez'); saveData('dez')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d15_fabricio_dez" step="0.01" oninput="calc('dez'); saveData('dez')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 15: <span id="total_d15_dez">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Dia 30</strong>
        <div class="inline-grid" style="margin-top:8px">
          <div>
            <label class="small">Michely</label>
            <input type="number" id="d30_michely_dez" step="0.01" oninput="calc('dez'); saveData('dez')">
          </div>
          <div>
            <label class="small">Fabricio</label>
            <input type="number" id="d30_fabricio_dez" step="0.01" oninput="calc('dez'); saveData('dez')">
          </div>
        </div>
        <p class="small" style="margin-top:8px">Total Dia 30: <span id="total_d30_dez">R$ 0,00</span></p>
      </div>

      <div class="earn-block">
        <strong>Extras</strong>
        <div style="margin-top:8px">
          <label class="small">Extra Michely</label>
          <input type="number" id="ext_michely_dez" step="0.01" oninput="calc('dez'); saveData('dez')">
        </div>
        <div style="margin-top:8px">
          <label class="small">Extra Fabricio</label>
          <input type="number" id="ext_fabricio_dez" step="0.01" oninput="calc('dez'); saveData('dez')">
        </div>
        <p class="small" style="margin-top:8px">Total Extra: <span id="total_ext_dez">R$ 0,00</span></p>
      </div>
    </div>

    <div class="totals">
      <p>Total Ganhos: <span id="total_ganhos_dez">R$ 0,00</span></p>
      <p>Soma Contas Dia 15: <span id="sum_bills_d15_dez">R$ 0,00</span></p>
      <p>Soma Contas Dia 30: <span id="sum_bills_d30_dez">R$ 0,00</span></p>
      <p>Total Pago: <span id="total_pago_dez">R$ 0,00</span></p>
      <p>Saldo Restante: <span id="saldo_dez">R$ 0,00</span></p>
    </div>

    <h3 style="margin-top:12px">Contas - Dia 15</h3>
    <table id="bills_d15_dez">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d15','dez')">Adicionar Conta (Dia 15)</button>

    <h3 style="margin-top:12px">Contas - Dia 30</h3>
    <table id="bills_d30_dez">
      <thead>
        <tr>
          <th>Categoria</th>
          <th>Descrição</th>
          <th>Valor</th>
          <th>Vencimento</th>
          <th>Status</th>
          <th>Ação</th>
        </tr>
      </thead>
      <tbody></tbody>
    </table>
    <button class="add-btn" onclick="addRow('d30','dez')">Adicionar Conta (Dia 30)</button>

    <h3>Gráficos</h3>
    <div class="charts-row">
      <div class="chart-wrap">
        <canvas id="pie_gvsg_dez"></canvas>
      </div>
      <div class="chart-wrap">
        <canvas id="pie_cat_dez"></canvas>
      </div>
    </div>
  </div>

</div> <!-- /wrap -->

<script>
/* === Config / categorias fixas === */
const descriptionOptions = ['Alimentação','Lazer','Combustível','Carro','Casa','Educação','Vestuário','Diversos'];
let chartInstances = {}; // Chart.js instances cached

function formatBR(v){
  return 'R$ ' + Number(v || 0).toLocaleString('pt-BR', {minimumFractionDigits:2, maximumFractionDigits:2});
}

/* === Theme handling === */
function toggleTheme(){
  const cur = document.documentElement.getAttribute('data-theme');
  const next = cur === 'dark' ? '' : 'dark';
  if(next) document.documentElement.setAttribute('data-theme', next);
  else document.documentElement.removeAttribute('data-theme');
  localStorage.setItem('theme', next);
}
function loadTheme(){
  const t = localStorage.getItem('theme') || '';
  if(t) document.documentElement.setAttribute('data-theme', t);
}

/* === Navigation months === */
function showMonth(m){
  document.querySelectorAll('.month-content').forEach(el=>el.classList.remove('active'));
  const target = document.getElementById('content_' + m);
  if(!target) return;
  target.classList.add('active');
  document.querySelectorAll('#tabs button').forEach(b=>b.classList.remove('active'));
  const btn = document.querySelector('#tabs button[data-month="'+m+'"]');
  if(btn) btn.classList.add('active');
  // recalculate to ensure content updates
  calc(m);
}

/* === Create new bill row === */
function addRow(day, month, data = null){
  const table = document.getElementById('bills_' + day + '_' + month);
  if(!table) return;
  const tbody = table.querySelector('tbody');
  const tr = document.createElement('tr');

  const selCategory = data && data.category ? data.category : descriptionOptions[0];
  const descText = data && data.desc_text ? data.desc_text : '';
  const valor = data && data.valor ? data.valor : '';
  const venc = data && data.venc ? data.venc : '';
  const status = data && data.status ? data.status : 'Pendente';

  tr.innerHTML = `
    <td>
      <select class="desc" onchange="saveData('${month}'); calc('${month}')">
        ${descriptionOptions.map(opt => `<option ${opt === selCategory ? 'selected' : ''}>${opt}</option>`).join('')}
      </select>
    </td>
    <td>
      <input class="desc_text desc-input" type="text" placeholder="Descrição (opcional)" value="${escapeHtml(descText)}" oninput="saveData('${month}');">
    </td>
    <td>
      <input class="valor" type="number" step="0.01" value="${valor}" oninput="calc('${month}'); saveData('${month}')" />
    </td>
    <td>
      <input class="venc" type="date" value="${venc}" oninput="saveData('${month}');" />
    </td>
    <td>
      <select class="status" onchange="calc('${month}'); saveData('${month}')">
        <option ${status==='Pendente'?'selected':''}>Pendente</option>
        <option ${status==='Pago'?'selected':''}>Pago</option>
        <option ${status==='Atrasada'?'selected':''}>Atrasada</option>
      </select>
    </td>
    <td class="actions"><button onclick="this.closest('tr').remove(); calc('${month}'); saveData('${month}')">Remover</button></td>
  `;
  tbody.appendChild(tr);
  saveData(month);
}

function escapeHtml(unsafe) {
  if(!unsafe && unsafe !== 0) return '';
  return String(unsafe).replace(/&/g, "&amp;").replace(/</g, "&lt;").replace(/>/g, "&gt;")
    .replace(/"/g, "&quot;").replace(/'/g, "&#039;");
}

/* === Calc totals and update charts === */
function calc(month){
  // earnings
  const d15_michely = parseFloat(document.getElementById('d15_michely_' + month).value) || 0;
  const d15_fabricio = parseFloat(document.getElementById('d15_fabricio_' + month).value) || 0;
  const total_d15 = d15_michely + d15_fabricio;
  document.getElementById('total_d15_' + month).innerText = formatBR(total_d15);

  const d30_michely = parseFloat(document.getElementById('d30_michely_' + month).value) || 0;
  const d30_fabricio = parseFloat(document.getElementById('d30_fabricio_' + month).value) || 0;
  const total_d30 = d30_michely + d30_fabricio;
  document.getElementById('total_d30_' + month).innerText = formatBR(total_d30);

  const ext_michely = parseFloat(document.getElementById('ext_michely_' + month).value) || 0;
  const ext_fabricio = parseFloat(document.getElementById('ext_fabricio_' + month).value) || 0;
  const total_ext = ext_michely + ext_fabricio;
  document.getElementById('total_ext_' + month).innerText = formatBR(total_ext);

  const total_ganhos = total_d15 + total_d30 + total_ext;
  document.getElementById('total_ganhos_' + month).innerText = formatBR(total_ganhos);

  // bills
  let sum_d15 = 0, sum_d30 = 0, paid = 0;
  document.querySelectorAll('#bills_d15_' + month + ' tbody tr').forEach(row => {
    const val = parseFloat(row.querySelector('.valor').value) || 0;
    const status = row.querySelector('.status').value;
    sum_d15 += val;
    if(status === 'Pago') paid += val;
  });
  document.getElementById('sum_bills_d15_' + month).innerText = formatBR(sum_d15);

  document.querySelectorAll('#bills_d30_' + month + ' tbody tr').forEach(row => {
    const val = parseFloat(row.querySelector('.valor').value) || 0;
    const status = row.querySelector('.status').value;
    sum_d30 += val;
    if(status === 'Pago') paid += val;
  });
  document.getElementById('sum_bills_d30_' + month).innerText = formatBR(sum_d30);

  document.getElementById('total_pago_' + month).innerText = formatBR(paid);
  const saldo = total_ganhos - paid;
  document.getElementById('saldo_' + month).innerText = formatBR(saldo);

  updateCharts(month);
}

/* === Update charts (pie: ganhos vs gastos ; pie: categorias) === */
function updateCharts(month){
  const total_ganhos = (parseFloat(document.getElementById('d15_michely_' + month).value) || 0)
    + (parseFloat(document.getElementById('d15_fabricio_' + month).value) || 0)
    + (parseFloat(document.getElementById('d30_michely_' + month).value) || 0)
    + (parseFloat(document.getElementById('d30_fabricio_' + month).value) || 0)
    + (parseFloat(document.getElementById('ext_michely_' + month).value) || 0)
    + (parseFloat(document.getElementById('ext_fabricio_' + month).value) || 0);

  const expenseMap = {};
  descriptionOptions.forEach(k => expenseMap[k] = 0);
  document.querySelectorAll('#bills_d15_' + month + ' tbody tr, #bills_d30_' + month + ' tbody tr').forEach(row => {
    const cat = row.querySelector('.desc').value;
    const val = parseFloat(row.querySelector('.valor').value) || 0;
    if(cat && expenseMap.hasOwnProperty(cat)) expenseMap[cat] += val;
  });
  const expenseValues = descriptionOptions.map(k => expenseMap[k]);
  const total_expenses = expenseValues.reduce((a,b)=>a+b,0);

  // Ganhos vs Gastos
  const gvsgId = 'pie_gvsg_' + month;
  if(document.getElementById(gvsgId)){
    const ctx = document.getElementById(gvsgId).getContext('2d');
    const key = 'gvsg_' + month;
    if(chartInstances[key]) chartInstances[key].destroy();
    chartInstances[key] = new Chart(ctx, {
      type: 'pie',
      data: {
        labels: ['Ganhos','Gastos'],
        datasets: [{ data: [total_ganhos, total_expenses], backgroundColor: ['#36A2EB','#FF6384'] }]
      },
      options: {
        plugins: {
          title: { display: true, text: 'Ganhos vs Gastos (R$)' },
          tooltip: {
            callbacks: {
              label: function(ctx){
                const lab = ctx.label || '';
                const val = ctx.parsed || 0;
                const total = (total_ganhos + total_expenses) || 1;
                const pct = ((val/total)*100).toFixed(2);
                return `${lab}: ${formatBR(val)} (${pct}%)`;
              }
            }
          }
        }
      }
    });
  }

  // Gastos por categoria
  const catId = 'pie_cat_' + month;
  if(document.getElementById(catId)){
    const ctx2 = document.getElementById(catId).getContext('2d');
    const key2 = 'cat_' + month;
    if(chartInstances[key2]) chartInstances[key2].destroy();
    chartInstances[key2] = new Chart(ctx2, {
      type: 'pie',
      data: {
        labels: descriptionOptions,
        datasets: [{ data: expenseValues, backgroundColor: ['#FF6384','#36A2EB','#FFCE56','#4BC0C0','#9966FF','#FF9F40','#C9CBCF','#7BC225'] }]
      },
      options: {
        plugins: {
          title: { display: true, text: 'Gastos por Categoria (R$)' },
          tooltip: {
            callbacks: {
              label: function(ctx){
                const lab = ctx.label || '';
                const val = ctx.parsed || 0;
                const pct = total_expenses > 0 ? ((val/total_expenses)*100).toFixed(2) : '0.00';
                return `${lab}: ${formatBR(val)} (${pct}%)`;
              }
            }
          }
        }
      }
    });
  }
}

/* === Persistence: save/load per month === */
function saveData(month){
  const earnings = {
    d15_michely: document.getElementById('d15_michely_' + month).value || '',
    d15_fabricio: document.getElementById('d15_fabricio_' + month).value || '',
    d30_michely: document.getElementById('d30_michely_' + month).value || '',
    d30_fabricio: document.getElementById('d30_fabricio_' + month).value || '',
    ext_michely: document.getElementById('ext_michely_' + month).value || '',
    ext_fabricio: document.getElementById('ext_fabricio_' + month).value || ''
  };
  localStorage.setItem('earnings_' + month, JSON.stringify(earnings));

  const bills15 = [];
  document.querySelectorAll('#bills_d15_' + month + ' tbody tr').forEach(row => {
    bills15.push({
      category: row.querySelector('.desc').value,
      desc_text: row.querySelector('.desc_text').value,
      valor: row.querySelector('.valor').value,
      venc: row.querySelector('.venc').value,
      status: row.querySelector('.status').value
    });
  });
  localStorage.setItem('bills_d15_' + month, JSON.stringify(bills15));

  const bills30 = [];
  document.querySelectorAll('#bills_d30_' + month + ' tbody tr').forEach(row => {
    bills30.push({
      category: row.querySelector('.desc').value,
      desc_text: row.querySelector('.desc_text').value,
      valor: row.querySelector('.valor').value,
      venc: row.querySelector('.venc').value,
      status: row.querySelector('.status').value
    });
  });
  localStorage.setItem('bills_d30_' + month, JSON.stringify(bills30));
}

/* === Load data at start === */
function loadData(){
  const months = ['jan','fev','mar','abr','mai','jun','jul','ago','set','out','nov','dez'];
  months.forEach(month => {
    const es = localStorage.getItem('earnings_' + month);
    if(es){
      try{
        const obj = JSON.parse(es);
        if(document.getElementById('d15_michely_' + month)) document.getElementById('d15_michely_' + month).value = obj.d15_michely || '';
        if(document.getElementById('d15_fabricio_' + month)) document.getElementById('d15_fabricio_' + month).value = obj.d15_fabricio || '';
        if(document.getElementById('d30_michely_' + month)) document.getElementById('d30_michely_' + month).value = obj.d30_michely || '';
        if(document.getElementById('d30_fabricio_' + month)) document.getElementById('d30_fabricio_' + month).value = obj.d30_fabricio || '';
        if(document.getElementById('ext_michely_' + month)) document.getElementById('ext_michely_' + month).value = obj.ext_michely || '';
        if(document.getElementById('ext_fabricio_' + month)) document.getElementById('ext_fabricio_' + month).value = obj.ext_fabricio || '';
      }catch(e){}
    }

    const b15 = localStorage.getItem('bills_d15_' + month);
    if(b15){
      try{
        const arr = JSON.parse(b15);
        arr.forEach(item => addRow('d15', month, item));
      }catch(e){}
    }

    const b30 = localStorage.getItem('bills_d30_' + month);
    if(b30){
      try{
        const arr = JSON.parse(b30);
        arr.forEach(item => addRow('d30', month, item));
      }catch(e){}
    }

    // small delay to ensure DOM elements exist
    setTimeout(()=>calc(month), 60);
  });
}

/* === Export / Import / Clear functions === */
function exportAll(){
  const months = ['jan','fev','mar','abr','mai','jun','jul','ago','set','out','nov','dez'];
  const out = {};
  months.forEach(m => {
    out['earnings_' + m] = JSON.parse(localStorage.getItem('earnings_' + m) || 'null');
    out['bills_d15_' + m] = JSON.parse(localStorage.getItem('bills_d15_' + m) || 'null');
    out['bills_d30_' + m] = JSON.parse(localStorage.getItem('bills_d30_' + m) || 'null');
  });
  out['_meta'] = { exported_at: new Date().toISOString(), theme: localStorage.getItem('theme') || '' };
  const blob = new Blob([JSON.stringify(out, null, 2)], {type: 'application/json'});
  const url = URL.createObjectURL(blob);
  const a = document.createElement('a');
  a.href = url;
  a.download = 'controle_financeiro_export_' + new Date().toISOString().slice(0,10) + '.json';
  document.body.appendChild(a);
  a.click();
  a.remove();
  URL.revokeObjectURL(url);
}

function importFile(e){
  const file = e.target.files[0];
  if(!file) return;
  const reader = new FileReader();
  reader.onload = function(evt){
    try{
      const data = JSON.parse(evt.target.result);
      // Overwrite localStorage keys present in file
      Object.keys(data).forEach(k => {
        if(k.startsWith('earnings_') || k.startsWith('bills_d15_') || k.startsWith('bills_d30_')){
          if(data[k] === null) localStorage.removeItem(k);
          else localStorage.setItem(k, JSON.stringify(data[k]));
        } else if(k === '_meta' && data[k] && data[k].theme) {
          if(data[k].theme) localStorage.setItem('theme', data[k].theme);
        }
      });
      alert('Importação concluída. A página será recarregada para aplicar os dados.');
      setTimeout(()=>location.reload(), 400);
    }catch(err){
      alert('Arquivo inválido: ' + err.message);
    }
  };
  reader.readAsText(file);
}

// Clear a single month
function clearMonth(month){
  if(!confirm('Confirma apagar todos os dados do mês ' + month + '?')) return;
  localStorage.removeItem('earnings_' + month);
  localStorage.removeItem('bills_d15_' + month);
  localStorage.removeItem('bills_d30_' + month);
  // remove charts instances to avoid stale objects
  ['gvsg_','cat_'].forEach(pref => {
    const key = pref + month;
    if(chartInstances[key]) { try { chartInstances[key].destroy(); } catch(e){} delete chartInstances[key]; }
  });
  // clear DOM rows
  const tb15 = document.querySelector('#bills_d15_' + month + ' tbody');
  const tb30 = document.querySelector('#bills_d30_' + month + ' tbody');
  if(tb15) tb15.innerHTML = '';
  if(tb30) tb30.innerHTML = '';
  // reset inputs
  const ids = ['d15_michely_','d15_fabricio_','d30_michely_','d30_fabricio_','ext_michely_','ext_fabricio_'];
  ids.forEach(id => { const el = document.getElementById(id + month); if(el) el.value = ''; });
  calc(month);
}

// clear all data
function clearAllData(){
  if(!confirm('Apagar TODOS os dados do aplicativo (localStorage)?')) return;
  localStorage.clear();
  location.reload();
}

/* === Init === */
window.addEventListener('DOMContentLoaded', () => {
  loadTheme();
  loadData();
  // show a sensible default month (outubro as before)
  showMonth('out');
});
</script>
</body>
</html>
