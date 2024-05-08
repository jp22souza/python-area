# python-area
import math

def calcular_area_altura(a, b, c):
    # Calcula a área usando a fórmula de Heron
    s = (a + b + c) / 2
    area = math.sqrt(s * (s - a) * (s - b) * (s - c))

    # Calcula a altura usando a fórmula da área do triângulo
    altura = (2 * area) / a

    return area, altura

def main():
    # Solicita ao usuário os comprimentos dos lados do triângulo
    a = float(input("Digite o comprimento do lado a do triângulo: "))
    b = float(input("Digite o comprimento do lado b do triângulo: "))
    c = float(input("Digite o comprimento do lado c do triângulo: "))

    # Calcula a área e a altura do triângulo
    area, altura = calcular_area_altura(a, b, c)

    # Exibe os resultados
    print(f"\nÁrea do triângulo: {area}")
    print(f"Altura do triângulo: {altura}")

if __name__ == "__main__":
    main()
