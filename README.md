Consulta 1: Devuelve el jugador que más partidas haya ganado.
void devolver_numero_1(char ganador [20])
{
  err=mysql_query(conn,"SELECT Ganador FROM Partidas GROUP BY Ganador ORDER BY COUNT(*) DESC LIMIT 1");
  printf(err);
  sprintf(ganador,"%S", err);
}
