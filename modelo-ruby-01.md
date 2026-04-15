pedido = {
  numero: 'PED-1025',
  status: 'pendente',
  total: 129.90
}

puts "Pedido #{pedido[:numero]} - status: #{pedido[:status]}"
puts "Total: R$ #{format('%.2f', pedido[:total])}"
