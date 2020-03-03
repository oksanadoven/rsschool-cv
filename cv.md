# **Oxana Solodovnik**
*Sometown, CA 43085*
*Tel.: 555-555-5555 | os@somedomain.com*
*LinkedIn | Portfolio Link*

## SUMMARY
> My primary goal is to apply my technical expertise all throughout the full software life cycle to ensure production and delivery of products and services that meet client specifications. Along with a competent software developing team, and with strong personal knowledge, skills, and experience in software engineering, I am positive that this goal can be achieved. My experience as junior software developer enhanced my abilities in designing, implementing, testing, and upgrading software. One of my objectives is to keep updated with the latest IT trends and technologies. I am confident that if given the opportunity, I can be a useful talent to the company.

## SKILLS AND COMPETENCES:
* Solid knowledge of C/C++
* Web Tools: JavaScript, jQuery, CSS, React, HTML, XHTML, XML, Bootstrap, MySQL, GitHub, REST
* Mobile Development: Java, Kotlin
* Expertise in back-end application design and development – working with RDBMS like Oracle, SQL Server etc

## CODE SNIPPETS

```
C
/* reverse Polish calculator */
int main() {
    int type, var = 0;
    double op2, sine, v; 
    double sin_param = PI / 180;
    char s[MAXOP];
    double variables[26];
    
    while ((type = getop(s)) != EOF) {
        switch (type) {
        case NUMBER:
            push(atof(s));
            break;
        case '+' :
            push((pop() + pop()));
            break;
        case '*':
            push(pop() * pop());
            break;
        case '-' :
            op2 = pop();
            push (pop () - op2);
            break;
        case '/':
            op2 = pop();
            if (op2 != 0.0)
                push(pop() / op2);
            else
                printf("error: zero divisor\n");
            break;
        case '%':
            op2 = pop();
            if (op2 != 0.0)
                push(fmod(pop(), op2));
            else
                printf("error: zero divisor\n");
            break;
        case 'p': /* Print top stack item without popping */
            printf("Top stack item = %.8g\n", val[--next_push_position]);
            return 0;
        case 'd': /* Duplicate top stack item without popping */
            duplicate();
            break;
        case 's': /* Swap two top stack items */
            swap();
            break;
        case 'c': /* Clear the stack */
            clear_stack();
            break;
        case 'n': /* get sin */
            sine = sin((pop() * sin_param));
            push(sine);
            break;
        case '~': /* get expotential of number */
            push(exp(pop()));
            break;
        case '`': /* get power of number */
            push(pow(pop(), pop()));
            break;
        case '=':
            pop();
            if(var >= 'A' && var <= 'Z')
            {
                variables[var-'A'] = pop();
            }
            else
            {
                printf("No variable name\n");
                break;
            }
        case '\n':
            printf ("\t%.8g\n", pop ());
            break;
        default:
            if(type >= 'A' && type <= 'Z')
            {
                push(variables[type-'A']);
            }
            else if (type == 'v')
            {
                push(v);
            }
            else
            {
                printf("error: unknown command %s\n", s);
            }
            break;
        }
        var = type;
    }

    return 0;
}
```
> For the full follow {the link](https://www.codepile.net/pile/j4GrQOoP)

## EDUCATION
* 42 School Silicon Valley
* CodeAcademy Web Development Certification
* Data Structures and Algorythms Course
