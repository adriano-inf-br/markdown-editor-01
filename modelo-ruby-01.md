class Pedido
  attr_reader :numero, :total

  def initialize(numero, total)
    @numero = numero
    @total = total
  end

  def aprovado?
    total >= 100.0
  end
end

pedido = Pedido.new('PED-2026-0001', 149.90)
puts "Pedido #{pedido.numero} aprovado? #{pedido.aprovado?}"
