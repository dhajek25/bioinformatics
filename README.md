# bioinformatics

https://rosalind.info/problems/locations/

https://github.com/ayigitdogan/Rosalind-Solutions

https://github.com/topics/rosalind-bioinformatics-challenge?o=desc&s=updated

**FUNCTION 1 (dna_nucleotides_count)**
Given: A DNA string **s** of length at most 1000 nt.

Return: Four integers counting the respective number of times that the symbols 'A', 'C', 'G', and 'T' occur in **s**


s = 'AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGC'

def dna_nucleotides_count(s):
    """
    Count the nucleotides (A, T, C, G) in the input string.

    Parameters:
    s (str): The input string to count nucleotides in.

    Returns:
    A view object of the dictionary's items. Each item is a tuple with a nucleotide and its count.

    Example:
    dna_nucleotides_count('AGCTTTTCATTCTGACTGCAACGGGCAATATGTCTCTGTGTGGATTAAAAAAAGAGTGTCTGATAGCAGC')
    dict_items([('A', 20), ('T', 21), ('C', 12), ('G', 17)])
    """

    nucl_dict = {'A': 0, 'T': 0, 'C': 0, 'G': 0}

    for e in s:
        if e in nucl_dict.keys():
            nucl_dict[e] += 1

    result = ''
    for key, value in nucl_dict.items():
        result += f"{key}: {value}\n"
    return result

result = dna_nucleotides_count(s)
print(result)
"""Hello Iam yellow"""