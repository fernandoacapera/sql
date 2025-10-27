
Arredonda para cima (para o próximo numero inteiro maior ou igual)
CEIL()

SELECT CEIL(4.2);   -- Resultado: 5
SELECT CEIL(7.0);   -- Resultado: 7
SELECT CEIL(-2.3);  -- Resultado: -2


**Arredonda para baixo** (para o inteiro menor ou igual).
FLOOR()

SELECT FLOOR(4.8);   -- Resultado: 4
SELECT FLOOR(-2.3);  -- Resultado: -3

**Arredonda para o número mais próximo**,podendo definir o número de casas decimais.

-- Arredonda para o inteiro mais próximo
SELECT ROUND(4.5);   -- Resultado: 5
SELECT ROUND(4.4);   -- Resultado: 4

-- Com casas decimais
SELECT ROUND(123.4567, 2);  -- Resultado: 123.46
SELECT ROUND(123.4567, 0);  -- Resultado: 123
SELECT ROUND(123.4567, -1); -- Resultado: 120
