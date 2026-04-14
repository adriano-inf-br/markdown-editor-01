class Pedido
  attr_reader :numero, :status, :total

  def initialize(numero, status, total)
    @numero = numero
    @status = status
    @total = total
  end

  def em_atraso?
    status == 'pendente'
  end
end

pedido = Pedido.new('1025', 'pendente', 129.90)
puts "Pedido ##{pedido.numero} em atraso? #{pedido.em_atraso?}"
