program MediaNotas;

var
  nota1, nota2, media: Real;

begin
  nota1 := 8.5;
  nota2 := 7.0;
  media := (nota1 + nota2) / 2;

  Writeln('Media final: ', media:0:2);

  if media >= 7.0 then
    Writeln('Situacao: aprovado')
  else
    Writeln('Situacao: recuperacao');
end.
