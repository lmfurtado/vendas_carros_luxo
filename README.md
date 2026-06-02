# 📊 Vendas XYZ — Power BI Report

An analytical sales report for a vehicle dealership built in Power BI, covering commercial performance, delivery costs, labor costs, and customer analysis broken down by manufacturer, model, and geographic region.

---

## 📁 File Structure

| File | Description |
|---|---|
| `Vendas_XYZ.pbix` | Main Power BI report file (~1.6 MB) |

---

## 📑 Report Pages

The report contains **7 pages**, all accessible from a central navigation menu:

| # | Page | Description |
|---|---|---|
| 1 | **Menu** | Main navigation page with shortcuts to all other sections |
| 2 | **Sales Report** | Sales overview: total sales, total cost, profit margin, YTD accumulation, map by state, and customer ranking |
| 3 | **Manufacturer Delivery** | Delivery cost analysis by manufacturer, model, state, and time evolution with accumulation |
| 4 | **Labor** | Labor costs by manufacturer and state, including 12-month moving average (MAT) and YTD |
| 5 | **Customers** | Customer ranking and segmentation by category, purchase frequency, and average ticket comparison |
| 6 | **Sales by Manufacturer** | Summary table of total sales grouped by manufacturer |
| 7 | **Video Wall** | Executive dashboard with high-impact visuals: treemap, word cloud, map, gauge, and line charts |

---

## 🗂️ Data Model

### Tables

#### `VendaCarros` — Main fact/dimension table
| Field | Description |
|---|---|
| `Fabricante` | Vehicle manufacturer/brand |
| `Modelo` | Vehicle model |
| `Cor` | Vehicle color |
| `Nome do Cliente` / `NomeCliente` | Customer name |
| `Categoria` | Product category |
| `Categoria de Clientes` | Customer segment |
| `Estado/País` | Geographic location of the sale |

#### `CalendarioDAX` — Date table
| Field | Description |
|---|---|
| `Date` | Full date |
| `Ano` | Year |
| `Mes` | Month (number) |
| `Mês Ano` | Month/year label for chart axes |

#### `Medidas` — DAX measures table
| Measure | Description |
|---|---|
| `Soma Vendas` | Total sales amount |
| `Custo Total` | Total aggregated cost |
| `Soma Custo Real` | Actual accumulated cost |
| `Margem de Lucro` | Profit margin (Sales − Costs) |
| `Custo Entrega` / `Soma Custo Entrega` | Delivery/logistics costs |
| `Custo Acumulado` | Accumulated cost over the period |
| `Mão de Obra` / `Soma Mão de Obra` | Labor costs |
| `Mão de Obra MAT` | 12-month moving average of labor costs |
| `Mão de Obra Ytd` | Year-to-date labor costs |
| `Mão de obra Acumulado` | Total accumulated labor costs |
| `Vendas Ytd` | Year-to-date sales (YTD) |
| `Vendas Acumulado` | Total accumulated sales |
| `Média Vendas` | Average ticket per customer |
| `Média Vendas Todos os Clientes` | Average ticket benchmark across all customers |
| `Frequência de Compras` | Number of orders per customer |
| `Rank Clientes` | Customer ranking by sales volume |
| `Data Último Pedido` | Date of the customer's most recent purchase |
| `Último Pedido Cliente x Último Pedido Geral` | Recency comparison: customer vs. overall last order |

---

## 🎛️ Available Filters (Slicers)

All analytical pages share the same interactive filters:

- **Manufacturer**
- **Model**
- **Color**
- **Date** (range)
- **Customer Name**
- **State/Country**

---

## 📊 Visual Types Used

| Visual | Where it's used |
|---|---|
| Card | KPIs: Total Sales, Total Cost, Profit Margin |
| Line Chart | Sales and cost trends over time |
| Clustered Column Chart | Comparisons by manufacturer, state, and period |
| Map | Sales and costs by state/country |
| Pivot Table | Breakdown by manufacturer, model, color, and customer |
| Table | Customer rankings and sales by manufacturer |
| Treemap | Sales share by manufacturer and model |
| Gauge | Total cost vs. total sales indicator |
| Word Cloud | Sales volume by vehicle model |
| Slicer | Interactive filters on all pages |
| Action Button | Page navigation |

> The **Word Cloud** is a custom visual (`WordCloud1447959067750`) imported via a `.pbiviz` file.

---

## 🖼️ Static Resources

The report includes supporting images for visual design:

- Thematic icons: sales, engineer, customer, delivery, and home
- Vehicle images (Jaguar) used as decorative backgrounds on report pages

---

## 🛠️ Requirements

- **Power BI Desktop** (recommended version: 2023.08 or later)
- The file was originally created on Power BI version `2023.08`

---

## 🚀 How to Use

1. Open `Vendas_XYZ.pbix` in **Power BI Desktop**.
2. Connect or refresh the data source as needed via **Home → Transform Data**.
3. Navigate between pages using the **Menu** on the first tab.
4. Use the **slicers** to filter by manufacturer, model, date range, customer, or region.
5. To publish to the Power BI service, click **Publish** and select the desired workspace.
