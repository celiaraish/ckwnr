from rich.console import Console
from rich.table import Table
from rich.panel import Panel
from rich import box
import pyfiglet

console = Console()

def load_list(filename):
    with open(filename, "r", encoding="utf-8") as f:
        return [line.strip() for line in f if line.strip()]

banner = pyfiglet.figlet_format("CREATOR", font="Doom")
console.print(f"[bold cyan]{banner}[/bold cyan]")
banner = pyfiglet.figlet_format("BY", font="slant")
console.print(f"[bold cyan]{banner}[/bold cyan]")
banner = pyfiglet.figlet_format("XBOOT", font="BIG")
console.print(f"[bold Green]{banner}[/bold Green]")

console.print(Panel.fit("[bold yellow]🔍 Pengecekan Address Winner[/bold yellow]", border_style="cyan"))


winner_file = "winner_list.txt"
my_file = "my_addresses.txt"


winner_list = load_list(winner_file)
my_addresses = load_list(my_file)


matches = []
for my_addr in my_addresses:
    start = my_addr[:6].lower()
    end = my_addr[-5:].lower()
    for winner in winner_list:
        if winner.lower().startswith(start) and winner.lower().endswith(end):
            matches.append(my_addr)
            break

if matches:
    console.print(f"[bold green]✅ {len(matches)} address kamu ADA di daftar pemenang[/bold green]\n")
    table = Table(title="Address Kamu yang Menang", box=box.ROUNDED, border_style="green")
    table.add_column("No", style="cyan", justify="right")
    table.add_column("Address", style="bold white")
    for i, addr in enumerate(matches, start=1):
        table.add_row(str(i), addr)
    console.print(table)
else:
    console.print("[bold red]❌ Tidak ada address kamu di daftar pemenang[/bold red]")
